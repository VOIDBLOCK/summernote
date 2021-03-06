Summernote editor extension for laravel-admin
======

这是一个`laravel-admin`扩展，用来将`Summernote`集成进`laravel-admin`的表单中

## 截图

![wx20180905-132310](https://user-images.githubusercontent.com/1479100/45072743-f1d92b00-b10e-11e8-9a51-9397fa4fb24e.png)

## 安装

```bash
composer require laravel-admin-ext/summernote
```

然后
```bash
php artisan vendor:publish --tag=laravel-admin-summernote
```

## 配置

在`config/admin.php`文件的`extensions`，加上属于这个扩展的一些配置
```php

    'extensions' => [

        'summernote' => [
        
            // 如果要关掉这个扩展，设置为false
            'enable' => true,
            
            // 编辑器的配置
            'config' => [
                
            ]
        ]
    ]

```

编辑器的配置可以到[Summernote文档](https://summernote.org/getting-started/)找到，比如配置语言和高度
```php
    'config' => [
        'lang'   => 'zh-CN',
        'height' => 500,
    ]
```

## 使用

在form表单中使用它：
```php
$form->summernote('content');
```

## 支持

如果觉得这个项目帮你节约了时间，不妨支持一下;)

![-1](https://cloud.githubusercontent.com/assets/1479100/23287423/45c68202-fa78-11e6-8125-3e365101a313.jpg)

License
------------
Licensed under [The MIT License (MIT)](LICENSE).
