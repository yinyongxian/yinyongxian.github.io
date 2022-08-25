---
layout: default
title: 批处理执行SQL Server语句
---

# 批处理执行SQL Server语句


存储到文件ExecuteSQL.cmd，修改对应值，双击即可执行。

``` cmd
@ECHO OFF 

SET dbhost=localhost
SET dbuser=admin
SET dbpasswd=password
SET dbName=DatabaseName

sqlcmd -S %dbhost% -U %dbuser% -P %dbpasswd% -d %dbName% -Q "sql"

ECHO.
ECHO Successed
::PAUSE

@ECHO Done! 
```
