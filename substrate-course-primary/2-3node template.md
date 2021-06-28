0000 node template 是为了让大家入门而弄出的最小可用单元。

0131 模块定义概览：第一行声明使用到的依赖。第二行声明一个关联类型，小写的trait是rust中的关键字。大写的是trait的名字。decl_storage声明runtime存储部分，even是声明事件，error是声明错误，module是声明用户可以调用的runtime的一些方法。最后implement module是符合rust语法的，这里声明一些虽然用户不能调用，但提供一些当前的pallet，模块的一些工具和方法。或者是其它模块可以调用的当前模块的一些方法。 ？？？
![](https://github.com/playdog-io/ph/blob/main/QQ%E6%88%AA%E5%9B%BE20210628171840.png)

0233 引入和定义关联类型：听不懂也没有关系，因为难度大。实操代码时就能理解了。  
在每一个pallet下面，都会声明一个trait。小写的trait是关键字，大写的是trait的名字。后面的冒号可以理解为继承自system这个pallet下面的trait。system是runtime中最基础的pallet，在大家自定义的pallet时几乎都会用到。在自定义的trait里，可以再自定义各种关联类型。关联类型是rust语言中的术语，可以理解为一个抽象类型？？？。每一个关联类型，如这里的type Origin，type Call，后面又是冒号，冒号后面跟的是各种trait的约束。在这里自定义这些关联类型是为了和其它模块，pallet产生交互。  
比如在这里我们自定义了一个block number。然后给它一些trait约束，比如可加可减这样的。后面在封装整个runtime时，我们可以赋予block number具体的类型，比如u32,u64,u128，或者直接使用hash值。只要它满足type blocknumber后面的各种trait约束。只需要在构造runtime时声明具体的类型就ok了。这是substrate高度模块化的体现之一。