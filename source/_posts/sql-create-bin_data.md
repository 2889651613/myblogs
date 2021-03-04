---
   title: 数据库生成大量测试数据
---

### mysql

  1. 通过load data infile "文件" replace into table "缓存table" (需要开启 mysql: secure_file_priv 权限)
  2. 通过缓存表和存储过程:
      - 储存表

            create table() ENGINE=MEMORY DEFAULT CHARSET=utf8mb4;

      - 存储过程

            create procedure '函数名'(INT  n int)
             begin
             declare i int default 1;
            while (i<=INT>) do
              需要插入的语句
              set i=i+1;
              end while;
            end;

### jpa

  1. jpa findAll() 方法查询大表数据的时候需要分页,如果部分也出现很耗时的问题

### mysql

### Oracle