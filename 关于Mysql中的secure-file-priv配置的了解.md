# 关于Mysql中的secure-file-priv配置的了解
Mysql对于数据的导出目录其实是可以进行配置限制的

**查看配置** 
show variables like '%secure_file_priv%';
在我本地的查询结果：

![](%E5%85%B3%E4%BA%8EMysql%E4%B8%AD%E7%9A%84secure-file-priv%E9%85%8D%E7%BD%AE%E7%9A%84%E4%BA%86%E8%A7%A3/%E5%85%B3%E4%BA%8EMysql%E4%B8%AD%E7%9A%84secure-file-priv%E9%85%8D%E7%BD%AE%E7%9A%84%E4%BA%86%E8%A7%A3/D0728B4A-A021-4ADA-8EBF-E2AB06259FFD.png)

当前的参数为NULL，目前我看到过三种参数，分别为NULL,””,_var_lib_mysql-files_

**参数含义**
NULL：完全限制导出
“” ：不限制导出
_var_lib_mysql-files_： 指导出为固定文件夹

说明：此参数是为了对mysql的导出目录进行限制，也可以在mysql的配置文件中对该参数进行自定义配置。