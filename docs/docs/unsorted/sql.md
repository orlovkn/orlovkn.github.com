https://www.tutorialspoint.com/mariadb/mariadb_select_database.htm
https://www.vultr.com/docs/cache-mysql-data-with-redis-and-php-on-ubuntu-20-04


## auth user
sudo mysql -u root -p


### add new user
UPDATE mysql.user SET authentication_string=PASSWORD('12345'), plugin='mysql_native_password' WHERE User='root' AND Host='localhost';    
FLUSH PRIVILEGES;

GRANT ALL PRIVILEGES ON *.* TO 'root'@'localhost';



sudo service mysql stop
sudo service mysql start



MariaDB [(none)]> SHOW DATABASES;
MariaDB [(none)]> use gwcontroller
MariaDB [gwcontroller]> SHOW TABLES;


### analize table
ANALYZE SELECT * FROM User;
EXPLAIN SELECT * FROM User;


SELECT u.username, CONCAT('$', FORMAT(sum(r.revenue) , 2)) revenue 
FROM revenue AS r 
LEFT JOIN users AS u ON r.id_user = u.id 
WHERE DATE(r.date) > (NOW() - INTERVAL 10 DAY) AND DATE(u.date) > (NOW() - INTERVAL 10 DAY) 
GROUP BY r.id_user 
ORDER BY revenue ASC;

+----------+---------+
| username | revenue |
+----------+---------+
| User3    | $120.40 |
| User1    | $14.80  |
| User2    | $28.00  |
+----------+---------+
3 rows in set (0.001 sec)


SELECT s.site_name, u.username, CONCAT('$', FORMAT(r.revenue , 2)) revenue
FROM revenue AS r 
LEFT JOIN sites AS s ON r.id_site = s.id 
LEFT JOIN users AS u ON u.id = r.id_user 
WHERE DATE(r.date) > (NOW() - INTERVAL 1 MONTH) 
ORDER BY r.revenue DESC;

+-----------+----------+---------+
| site_name | username | revenue |
+-----------+----------+---------+
| Web4      | User3    | $120.40 |
| Web4      | User2    | $15.40  |
| Web3      | User1    | $14.80  |
| Web4      | User2    | $12.60  |
+-----------+----------+---------+
4 rows in set (0.001 sec)

SELECT date, CONCAT('$', FORMAT(revenue, 2)) revenue, impressions 
FROM revenue 
WHERE id_user = 2 AND DATE(date) > (NOW() - INTERVAL 7 DAY) 
ORDER BY date DESC;

+------------+---------+-------------+
| date       | revenue | impressions |
+------------+---------+-------------+
| 2021-03-15 | $12.60  |          10 |
+------------+---------+-------------+
1 row in set (0.001 sec)



		$sql = "SELECT 
					p.ID AS PAGE_ID,
					COUNT(DISTINCT w.UID_ID) AS CNT
				FROM ww_metrics_way w, ww_metrics_users u, ww_metrics_pages p 
				WHERE u.ISNEW IN (0,1) ".$where."
					AND u.ID = w.UID_ID
					AND p.ID = w.PAGE_ID
				GROUP BY p.ID
				";


+------------+---------+-------------+

