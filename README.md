# bootstrap-table
中文帮助文档：[http://bootstrap-table.wenzhixin.net.cn/zh-cn/documentation/](http://bootstrap-table.wenzhixin.net.cn/zh-cn/documentation/)

英文帮助文档：[http://bootstrap-table.wenzhixin.net.cn/documentation/](http://bootstrap-table.wenzhixin.net.cn/documentation/)

原始GitHub地址：[https://github.com/wenzhixin/bootstrap-table](https://github.com/wenzhixin/bootstrap-table)

本次修改内容：

在columns数组的对象中增加dbColumn属性，用来表示此字段在数据库中的列名，主要是在排序的时候起作用。如果field的值与数据库中字段名不一致，但是需要对这一列进行排序的时候，就需要加上dbColumn字段，框架会自动以dbColumn优先，如果不配置dbColumn则会以field进行排序。

例如：

需要对编码字段进行排序，分页的JSON以orderCode为节点，但是数据库的字段为order_code，所以需要配置dbColumn

{title: '编码', field: 'orderCode', dbColumn:"order_code", align: 'center', valign: 'middle', sortable:true}