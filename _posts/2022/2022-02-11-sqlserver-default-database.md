---
layout: default
title: SQL Server Default Database
---

# SQL Server Default Database

设置登录SQL Server时默认的数据库，减少不必要切换：默认数据库 $\Rightarrow$ 想要的数据库。

```SQL
DECLARE @loginText nvarchar(256)
SELECT @loginText = SUSER_NAME()
EXEC sp_defaultdb  @loginame =  @loginText , @defdb =  'DatabaseName'
```
