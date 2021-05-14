install

https://tecadmin.net/install-redis-ubuntu/
https://redis.io/download


sudo systemctl restart redis-server.service
sudo systemctl status redis-server.service

## to start redis
redis-cli

## list of commands
https://redis.io/commands

SET name "Somename"
GET name
EXISTS name
DEL name


### time of a life
EXPIRE session 10


```
127.0.0.1:6379> SET counter 1000
OK
127.0.0.1:6379> INCRBY counter 33
(integer) 1033
127.0.0.1:6379> GET counter
"1033"
127.0.0.1:6379> DECR counter
(integer) 1032
```


### hashes
127.0.0.1:6379> HMSET user id 45 name "John"
OK
127.0.0.1:6379> HGET id
(error) ERR wrong number of arguments for 'hget' command
127.0.0.1:6379> HGET user id
"45"
127.0.0.1:6379> HGET user name
"John"
127.0.0.1:6379> HGETALL user
1) "id"
2) "45"
3) "name"
4) "John"


### lists
127.0.0.1:6379> LPUSH newlist 10
(integer) 1
127.0.0.1:6379> RPUSH newlist 12
(integer) 2
127.0.0.1:6379> GET newlist
(error) WRONGTYPE Operation against a key holding the wrong kind of value
127.0.0.1:6379> LRANGE newlist 0 1
1) "10"
2) "12"
127.0.0.1:6379> LPUSH newlist 55
(integer) 3
127.0.0.1:6379> LRANGE newlist 0 1
1) "55"
2) "10"
127.0.0.1:6379> LRANGE newlist 0 2
1) "55"
2) "10"
3) "12"
127.0.0.1:6379> LRANGE newlist 0 3
1) "55"
2) "10"
3) "12"
127.0.0.1:6379> LTRIM newlist 0 1
OK
127.0.0.1:6379> LRANGE newlist 0 3
1) "55"
2) "10"
127.0.0.1:6379> RPOP newlist 0 1
(error) ERR wrong number of arguments for 'rpop' command
127.0.0.1:6379> RPOP 1
(nil)
127.0.0.1:6379> LRANGE newlist 0 3
1) "55"
2) "10"
127.0.0.1:6379> 


### Redis Sets + Sorted Sets
127.0.0.1:6379> SADD ourset 1 2 3 4 5
(integer) 5
127.0.0.1:6379> SMEMBERS ourset
1) "1"
2) "2"
3) "3"
4) "4"
5) "5"
127.0.0.1:6379> SADD ourset 1 2 3
(integer) 0
127.0.0.1:6379> SMEMBERS ourset
1) "1"
2) "2"
3) "3"
4) "4"
5) "5"
127.0.0.1:6379> SISMEMBER ourset 
(error) ERR wrong number of arguments for 'sismember' command
127.0.0.1:6379> SISMEMBER ourset 5
(integer) 1
127.0.0.1:6379> SISMEMBER ourset 54
(integer) 0
127.0.0.1:6379> ZADD team 50 "Wizzards"
(integer) 1
127.0.0.1:6379> ZADD team 40 "Cavaliers"
(integer) 1
127.0.0.1:6379> ZRANGE team 0 1
1) "Cavaliers"
2) "Wizzards"
