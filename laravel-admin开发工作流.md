# larave-admin 开发工作流

## 添加控制器

> 我们使用如下Artisan命令为User模型创建对应的控制器：
```
php artisan admin:make UserController --model=App\\User
```
> win写法
 ```
php artisan admin:make UserController --model=App\User 
 ```

## 添加路由
> 在app/Admin/routes.php中添加路由：
```
$router->resource('users', UserController::class);
```

## 添加左侧菜单项
> 打开http://localhost/admin/auth/menu，添加菜单链接并刷新页面，就会看到左侧菜单条。

## 构建格子和表单
> 接下来要做的是打开app/Admin/Contollers/UserController.php，找到grid和form方法，并通过model-grid和model-form编写自己的代码。
