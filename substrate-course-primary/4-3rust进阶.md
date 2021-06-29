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

0800 把泛型和trait结合起来，让泛型有某种约束，满足这些约束的类型才可以使用。换句话说就是当编译器尝试替换泛型时，具体的类型必须有trait定义的功能或行为，也就是说这个具体类型实现了这个trait。  
0830 例子 重点！！！  定义一个函数notify，它接受一个参数item，item的类型是一个泛型的引用。这个泛型必须满足Summary这个trait。这里通过 冒号Summary 进行接口的约束，叫做trait bond。约束比较简单时可以使用下面的形式。
![](https://github.com/playdog-io/ph/blob/main/QQ%E6%88%AA%E5%9B%BE20210629195936.png)
0939 代码示例:
```
fn main(){
        let tweet = Tweet {
            author: String::from("Kaichao"),
            text: String::from("hello world"),
        };
        notify(&tweet);
}

pub trait Summary {
    fn summarize(&self) -> String;
}

struct Tweet {
    author: String,
    text: String,
}

impl Summary for Tweet {
    fn summarize(&self) -> String {
        format!("{},{}",self.author, self.text)
    }
}

pub fn notify<T: Summary>(item: &T) {
    println!("{}", item.summarize());
}
```

1103 多个参数时，trait bound可以保证类型一致  
1141 多个类型参数时，使用 +   
1156 where关键字

1244 变量的生命周期  
1357 引用的生命周期  
1635 引用的生命周期：缺省规则  
1810 结构体的生命周期  
1854 静态生命周期 static