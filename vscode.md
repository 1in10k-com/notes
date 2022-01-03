<details>
  <summary><mark><font color=darkred>paste image插件</font></mark></summary>
  <pre><code>
  此插件默认快捷键与网易词典快捷键有冲突，需要设置下。设置为ctrl shift z 后会跟qq快捷键有冲突，可以取消掉此qq快捷键。
  
  （修改方式为ctrl shift p 打开命令栏，搜索paste image，再点击修改。）

  注意在``` ```中不会显示图片只会显示链接
  </code></pre>
</details>

<details>
  <summary><mark><font color=darkred>vscode解决 windows换行crlf与lf冲突 ^M问题</font></mark></summary>
  <pre><code>
  https://blog.csdn.net/glorydx/article/details/110958739
 一劳永逸的解决方法
如果你所有的同事都是使用windows系统，
vscode 点击文件 --》首选项 --》 设置 --》 搜索 eol，改变eol为\n(指lf)或者改为(\r\n)，有一个统一的标准就好了。

git在维护版本库的时候统一使用的是LF，这样就可以保证文件跨平台的时候保持一致。
在Linux下默认的换行符也是LF，那也就不存在什么问题。
在Windows下默认的换行符是CRLF，那么我们需要保证在文件提交到版本库的时候文件的换行符是LF，通常来说有两种方法：

如果你同事中有使用其它系统开发的
你需要先执行上面的操作，再行 以下代码才能解决

 git config --global core.autocrlf false
  </code></pre>
</details>
