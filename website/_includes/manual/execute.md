## Execute

 `Execute` executes any SQL statement. The statement is specified as the first fixture parameter. There are no additional rows required for this command.

 You can use query parameters in the DB-specific syntax (eg. `@paramname` for SQLServer and MySQL, and `:paramname` for Oracle). Currently, all parameters are used as inputs, and there is no option to persist any statement outputs.

    !3 to execute statements, use the 'execute' command

    |Execute Ddl|Create table Test_DBFit(name varchar(50), luckyNumber int)|

    |Execute|Insert into Test_DBFit values ('Obi Wan',80)|
     
    |Set parameter|name|Darth Maul|

    |Execute|Insert into Test_DBFit values (@name,10)|

    |Query|Select * from Test_DBFit|
    |Name|Lucky Number|
    |Darth Maul|10|
    |Obi Wan|80|

    |Execute Ddl|Drop table Test_DBFit|

