---
layout: post
title: Django字段类型
descripyion: Django字段类型和选项
date: 2022-04-19
tag: Django
---

# Django字段类型

**Django创建字段时，需要定义数据类型，其中常用的数据类型如下：**

| 类型                  | 说明       | 描述                                                         |
| --------------------- | ---------- | :----------------------------------------------------------- |
| **AutoField**         | 自增字段   | 如果不显示指定主键，django每次都会自动新建一个自增字段（并设置为主键） |
| **CharField**         | 字符串字段 | 参数max_length表示最大字符个数                               |
| **IntegerField**      | 整型字段   | -2147483648 到 2147483647                                    |
| **SmallIntegerField** | 整型字段   | 小整数时一般会用到,-32,768到+32,767                          |
| **DecimalField**      | 浮点数字段 | 必须属性 max_digits=总位数(不含符号)  decimal_places=小数位数 |
| **FloatField**        | 浮点数字段 | 浮点数，参数同上                                             |
| **BooleanField**      | 布尔型字段 | 值为True或False                                              |
| **NullBooleanField**  |            | 支持Null、True、False三种值。                                |
| **TextField**         | 字符串字段 | 容量很大的文本字段，一般超过4000个字符时使用                 |
| **EmailField**        | 邮箱字段   | 可以通过EmailValidator验证邮箱格式，不接受max_length参数     |
| **DateField**         | 日期字段   | 1)参数auto_now表示每次保存对象时，自动设置该字段为当前时间，默认为false2) 参数auto_now_add表示当对象第一次被创建时自动设置当前时间，默认为false |
| **DateTimeField**     | 日期字段   | 功能类似DateField，支持同样的参数                            |
| **TimeField**         | 日期字段   | 参数同DateField                                              |
| **FileField**         |            | 上传文件字段                                                 |
| **ImageField **       |            | upload_to='type', whith_fiel= , height_field= 继承于FileField，对上传的内容进行校验，确保是有效的图片（jpg、png） |
| **URLField**          | URL字段    | verify_exists=True(默认)                                     |
| **IntegerField**      | 主键       | 主键，它同AutoField一样，唯一的差别就是不自增                |

| 选项名                            | 描述                                                         |
| --------------------------------- | ------------------------------------------------------------ |
| **default**                       | 设置默认值                                                   |
| **verbose_name**                  | 用于指定字段名称                                             |
| **primary_key**                   | 若为True，则该字段会成为模型的主键字段，默认值是False，一般作为AutoField的选项使用。 |
| **choices**choices=字段名_choices | 配置字段的choices后，在admin页面上就可以看到对应的选项展示，choice显示中文可以使用 "get_字段名_display()" |
| **unique**                        | 如果为True, 这个字段在表中必须有唯一值，默认值是False        |
| **db_index**                      | 若值为True, 则在表中会为此字段创建索引，默认值是False        |
| **db_column**                     | 字段的名称，如果未指定，则使用我们定义的Field对应数据库中的字段名称 |
| **null**                          | 如果为True，表示允许为空，默认值是False                      |
| **blank**                         | 如果为True，则该字段允许为空白，默认值是False                |