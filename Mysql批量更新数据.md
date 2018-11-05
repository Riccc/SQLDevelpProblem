# Mysql批量更新数据
 insert into TABLE_NAME (id,column1,column2,…) values (1,xx,xxx,…),(2,xx,xxx,…) on duplicate key update id = values(id),column1 = values(column1), column2 = values(column2),….

需要注意的是要使用表主键来作为数据更新的对应标准，更新字段与值的顺序对应，且更新column列表里必须包含所有的表非空字段，若不想对非空字段进行更新，可直接在对应的value位置置为空字符。