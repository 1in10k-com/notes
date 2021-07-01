<details>
  <summary><mark><font color=darkred>不能在函数外let定义变量。</font></mark></summary>
  <pre><code>  
fn main() {
//这里两个let如果放在函数外面就会报错
    let shili1 = Struct1 {
        cnname: String::from("cnname1"),
        engname: String::from("engname1"),
    };
    
    let shili2 = Struct2{
        cnname: String::from("cnname2"),
        jpname: String::from("jpname1"),
    };

    println!("Hello, world!");
    println!("this is 4 shili1, {}", shili1.trash());
    println!("this is 4 shili2, {}", shili2.trash());
}

pub trait Trait {
    fn trash(&self) -> String;
}

pub struct Struct1 {
    pub cnname: String,
    pub engname: String,
}

pub struct Struct2 {
    pub cnname: String,
    pub jpname: String,
}

impl Trait for Struct1 {
    fn trash(&self) -> String {
        format!("{}:{}", &self.cnname, &self.engname)
    }
}

impl Trait for Struct2 {
    fn trash(&self) -> String {
        format!("{}:{}", &self.cnname, &self.jpname)
    }
}
  </code></pre>
</details>