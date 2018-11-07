# 创建数据库迁移表
```
 php artisan make:migration create_students_table --create=students 
 php artisan make:migration create_student_class_outs_table --create=student_class_outs
 php artisan make:migration create_student_class_ins_table --create=student_class_ins
 php artisan make:migration create_student_class_nows_table --create=student_class_nows
 php artisan make:migration create_student_follows_table --create=student_follows
 php artisan make:migration create_student_moneys_table --create=student_moneys
 php artisan make:migration create_prepays_table --create=prepays
 ```
 
### 重新生成数据表
```
php artisan migrate:refresh
```

# 创建model
```
php artisan make:model Student
php artisan make:model StudentClassOut
php artisan make:model StudentClassIn
php artisan make:model StudentClassNow
php artisan make:model StudentClassFollow
php artisan make:model StudentMoney
php artisan make:model Prepay
```

# 数据填充

### 生成迁移文件

```
 php artisan make:seeder UsersTableSeeder
 php artisan make:seeder StudentsTableSeeder
 php artisan make:seeder StudentClassOutSeeder
 php artisan make:seeder StudentClassInSeeder
 php artisan make:seeder StudentClassNowSeeder
 php artisan make:seeder StudentClassFollowSeeder
 php artisan make:seeder StudentMoneySeeder
 php artisan make:seeder PrepaySeeder
```

### 在DatabaseSeeder的run方法中添加要执行数据填充的类

```
$this->call(UsersTableSeeder::class);
$this->call(StudentsTableSeeder::class);
$this->call(StudentClassOutSeeder::class);
$this->call(StudentClassInSeeder::class);
$this->call(StudentClassNowSeeder::class);
$this->call(StudentClassFollowSeeder::class);
$this->call(StudentMoneySeeder::class);
$this->call(PrepaySeeder::class);
```

### 填充命令 

```
php artisan db:seed
```


