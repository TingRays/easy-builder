# 关于数据迁移的一些使用
>
> 首先，使用构建器命令，会自动生成相关migration文件。
> 
> ```shell
> php artisan builder:package {your-table-name-without-db-prefix} //构建器命令
> ```
>
> 无需额外使用 `php artisan make:migration create_users_table` 命令。


## 迁移的使用方法

1. 在 `database\migrations` 目录里面， `abnermouke` 代表不同功能模块的迁移文件
2. 建议使用迁移命令 `php artisan migrate --path=database\migrations\fillings`,在 `path`后跟上`fillings`里面的文件路径。
3. 新增的功能模块迁移文件需要在  `database\migrations\fillings\xxxx_xx_xx_xxxxx_create_fillings_table.php` 中的 `up` 方法中增加后，使用建议的迁移命令才会生效。


注意：表 `migrations` 中的记录也会是影响执行迁移结果的。