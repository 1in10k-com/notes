0000 node template 是为了让大家入门而弄出的最小可用单元。

0131 第一行声明使用到的依赖。第二行声明一个关联类型，小写的trait是rust中的关键字。大写的是trait的名字。decl_storage声明runtime存储部分，even是声明事件，error是声明错误，module是声明用户可以调用的runtime的一些方法。最后implement module是符合rust语法的，这里声明一些虽然用户不能调用，但提供一些当前的pallet，模块的一些工具和方法。或者是其它模块可以调用的当前模块的一些方法。 ？？？
![](https://github.com/playdog-io/ph/blob/main/QQ%E6%88%AA%E5%9B%BE20210628171840.png)
