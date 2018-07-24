## 1.关于数据库
    //创建数据库
        create database h_test;        
    //查看数据库
        show databases;  
    //查看数据库信息    
        show create database h_test;
    //修改数据库的编码，可使用上一条语句查看是否修改成功
        alter database h_test default character set gbk collate gbk_bin;      
    //删除数据库
        drop database h_test;
    //综上，可以直接创建数据库且设置编码方式
        CREATE DATABASE h_test DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;

---

## 2.关于数据表
    //首先选定操作的数据库
        use h_test;
    //创建表student
        create table student(
          id  int(11),
          name  varchar(20),
          age int(11)
        );
    //查看数据表
        show tables;
    //查看数据表信息，后面加上参数/G可使结果更加美观
        show create table student;
    //查看表的的字段信息
        desc student;
    //修改表名
        alter table student rename [to] h_student;
    //修改字段名
        alter table h_student change name stu_name varchar(20);
    //修改字段的数据类型
        alter table h_student modify id int(20);
    //添加字段
        alter table h_student add grade float;
    //删除字段
        alter table h_student drop grade;
    //修改字的位置
        alter table h_student modify stu_name varchar(20) first;
        alter table h_student modify id int(11) after age;
    //删除数据表
        drop table h_student;

----

## 3.表约束

| 约束条件 | 说明 |
|---------|------|
|PRIMARY KEY|主键约束，用于唯一标识一条记录|
