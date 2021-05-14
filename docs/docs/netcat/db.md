## Класс nc_db_table

### Инициализация
```
nc_db_table::make('Message2000')
```

### Поля и сортировка
```
select($select = '*')
select('Message_ID, Name')
```

Вывод на экран
```
$objects = nc_db_table::make('Message2000')
                      ->select('Message_ID, Name')
                      ->get_result();
print_r($objects);
```

Сортировка результата, по умолчанию ASC
```
order_by($field, $type = ‘ASC’)
```

### Примеры
```
$result = nc_db_table::make('Message2000')
                     ->select()
                     ->order_by('Message_ID')
                     ->get_result();
```

Можно использовать несколько последовательных вариантов сортировки
```
$result = nc_db_table::make('Message2000')
                     ->order_by('Message_ID', 'DESC')
                     ->order_by('Caption')
                     ->get_result();
```

### Условия для запроса
```
where_id($id)
where($key, $operator = null, $value = null)
or_where($key, $operator = null, $value = null)
or_where_id($operator = null, $value = null)
where_in($key, $values)
where_in_id($values)
or_where_in($key, $values)
or_where_in_id($values)
```

### Примеры
```
$objects = nc_db_table::make('Message2000')
                      ->select()
                      ->where('Checked', 1)// WHERE `Checked` = 1
                      ->where('Message_ID', '>', 8)// WHERE `Message_ID` > 8
                      ->or_where('Message_ID', 3)// OR WHERE `Message_ID` = 3
                      ->get_result();
```
Для выборки конкретных разделов:
```
$objects = nc_db_table::make('Message2000')
                      ->select()
                      ->where_in('Message_ID', array(3, 4, 10))// WHERE `Message_ID` IN (3,4,10)
                      ->get_result();
```
Здесь в качестве оператора ($operator) может использоваться символы сравнения (>, <), неравенства (!=) и т. д.

### Прочие модификаторы
```
group_by($field) — группировка данных по полю
limit($limit) — лимитировать количество объектов для вывода
as_object() — вывод в виде объектов
as_array() — вывод в виде массива
index_by($key) — сортировать массив по ключу
index_by_id() — сортировать массив по id
get_result() — результат запроса 
get_row($where_key_value = null) — вывод строки в соответствии с запросом
get_value($field = null)
get_list($index_by, $values = null) — возвращает результат запроса в виде массив [key => value(s)]
```
```
$model->get_list('name') // Вернет массив вида ((id=>name), …)
$model->get_list('custom_id', 'name') // Вернет массив вида ((custom_id=>name), …)
$model->get_list(array('name', 'notice')) // Вернет массив вида ((id=>[name=>, notice=>]), …)
$model->get_list('login', array('name', 'notice')) // Вернет массив вида ((login=>[name=>, notice=>]), …)
```

### count_all — количество элементов
```
// подсчитать общее количество записей
$count_all = nc_db_table::make('Message8')->count_all();

// добавим селектор — только включенные объекты
$count_1   = nc_db_table::make('Message8')->where('Checked', 1)->count_all();
```

### Примеры
```
// вывести все записи
// таблица Message2000
$objects = nc_db_table::make('Message2000')
                      ->select()
                      //->select('Message_ID, Name')// вариант
                      ->where('Checked', 1)
                      ->order_by('Message_ID', 'DESC')
                      ->order_by('Name')
                      ->as_object()// as_array
                      ->get_result();

//print_r($result);

foreach ($objects as $obj) {
    echo $obj->caption . "<br>";
}
```

```
// аналогично можем вытащить данные из другой таблицы базы
$subdivisions = nc_db_table::make('Subdivision')
                           ->select()
                           //->select('Subdivision_ID, Subdivision_Name')// вариант
                           ->where('Checked', 1)
                           ->order_by('Subdivision_ID', 'DESC')
                           ->as_object()// as_array
                           ->get_result();

//print_r($result);

foreach ($subdivisions as $subs) {
    echo $subs->Subdivision_Name . "<br>";
}
```