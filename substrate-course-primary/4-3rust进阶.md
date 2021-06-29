0000 泛型，trait和生命周期

0018 为什么使用泛型  
0114 泛型-结构体的例子  
0245 泛型枚举例子  
0328 泛型函数签名例子  
0624 使用泛型的注意点

0655 trait：trait抽象了某种功能或行为，它告诉编译器这个类型可以实现这样的功能，不同的类型都可以具有这样的行为或功能。  
0720 trait的定义（更像是举例），定义了一个trait，名字叫Summary，它包含一个方法叫summarize，它没有一个默认的实现。也就是说实现Summary trait的类型必须实现summarize这样的方法。！！！  
0740 另一个例子是同样定义了Summary这个trait，但是给summarize这个函数定义了一个默认实现。那实现Summary trait的类型，如果这样的类型希望使用默认实现的话。那他就不需要使用summarize这样的方法。！！！？？？
![](https://github.com/playdog-io/ph/blob/main/QQ%E6%88%AA%E5%9B%BE20210629161821.png)
