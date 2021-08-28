
# Migration In Laravel With Command Line

Create table, add column, rename, drop column etc. you can 
perform with command line. From these tutorial you can easily 
work on migration of Laravel with command line. This is the 
good idea to work on database through migration.



## Commands For Migration
#### [Create model and migration file in single command]()


```bash
  php artisan make:model ModelName -m
```

 #### [Add new column to an existing table]()

  
```bash
  php artisan make:migration add_columName --table="tablename"
```




#### [Rename column name from table]()

Use below code

```bash
php artisan make:migration rename_columnName --table="tablename"
```

**In Migration File :**  Add below code on migration file in 
`up function`. Suppose if I want to rename `from_time` to 
`pickup_from_time`.
  


```bash
$table->renameColumn('from_time','pickup_from_time');
```

Add below code on migration file in `down function`

```bash
$table->renameColumn('pickup_from_time','from_time');
```


#### [Drop column name from table]()

Use below code

```bash
php artisan make:migration drop_columnName --table="tablename"
```

**In migartion file :** Add below code on migration file in 
`up function`. 

```bash
$table->dropColumn('columName');
```



**NOTE :-** If you did mistake in migration process you can delete migration files, model files. And also clear data from migration table
	(Only which file you created) and drop the table from database.
