# 表的分割

## 总结思路：
* lagou_city表:
	> 字段有编号，省，市，县或区，编号是主键，先对区域表进行查询获取id相同的列和
	等级数，1代表省，2代表市，3代表县，查等级为2和1的数据作为条件，从而获得省
	对应的市和市对应的县，最后插入数据；
* lagou_company表:
	> 从原表中查出公司表对应的字段，通过“as 查询的数据 from 原表名”语法获取数据
	在创建表的同时插入数据；
* lagou_position表：
	> 先查出position表中的district字段的为空或不为空的数据，通过union all 关键字将数据
	组合到一起，最后将所有数据插入到lagou_position表中；
