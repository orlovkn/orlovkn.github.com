## laravel
### installation

1.
```
composer global require laravel/installer
```

2.
```
cd ~
sudo nano .bashrc
export PATH="$PATH:$HOME/.config/composer/vendor/bin"
source ~/.bashrc
```

3.
```
laravel new application
```

4.
```
cd application/
php artisan key:generate --ansi
```

5. 
```
php artisan serve
```


================================
Request::all()



$title=ucwords($this->faker->words(4,true));
$slug=Str::slug($title,'-');
return [
    'user_id' => User::factory(),
    'title'=> $title,
    'description'=> $this->faker->paragraph(5),
    'slug'=>$slug,
];

================================

@php
switch ($width) {
    case '48':
        $width = 'w-48';
        break;
}
@endphp


{{ $width }}

// $post = cache()->remember("posts.{$slug}", now()->addMinutes(), fn() =>$path;


// $post = cache()->remember("posts.{$slug}", now()->addMinutes(), function() use ($path) {
$post = cache()->remember("posts.{$slug}", 5, function() use ($path) {
	return $path;
})