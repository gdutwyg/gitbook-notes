# gitbook的使用

### 1. 通过GitBook Editor方式
可视化编辑器   
[Editor下载地址](https://www.gitbook.com/editor)    
[Editor github地址](https://github.com/GitbookIO/editor-legacy)  

### 2. 通过nodejs方式
命令行方式
- 确定安装好了node和npm
- `gitbook init` 我们首先先创建 SUMMARY.md和README.md两个文件
    
    ```sh
    book/
    ├── README.md   是对书籍的简单介绍
    └── SUMMARY.md  是书籍的目录结构
    ```

    README.md
    ```
    This is a book powered by [GitBook](https://github.com/GitbookIO/gitbook).
    ```

    SUMMARY.md
    ```sh
    * [Introduction](README.md)
    * [Chapter1](chapter1/README.md)
      * [Section1.1](chapter1/section1.1.md)
      * [Section1.2](chapter1/section1.2.md)
    * [Chapter2](chapter2/README.md)
    ```

创建了这两个文件后，使用 `gitbook init`，它会为我们创建 SUMMARY.md 中的目录结构 

- `gitbook init` 之后生成gitbook执行`gitbook serve` ,生成一个_book文件夹

现在，可以用浏览器打开 http://127.0.0.1:4000 查看书籍的效果

### 3. 附上gitbook常用指令

```
- gitbook init //初始化目录文件
- gitbook help //列出gitbook所有的命令
- gitbook --help //输出gitbook-cli的帮助信息
- gitbook build //生成静态网页
- gitbook serve //生成静态网页并运行服务器
- gitbook build --gitbook=2.0.1 //生成时指定gitbook的版本, 本地没有会先下载
- gitbook ls //列出本地所有的gitbook版本
- gitbook ls-remote //列出远程可用的gitbook版本
- gitbook fetch 标签/版本号 //安装对应的gitbook版本
- gitbook update //更新到gitbook的最新版本
- gitbook uninstall 2.0.1 //卸载对应的gitbook版本
- gitbook build --log=debug //指定log的级别
- gitbook builid --debug //输出错误信息

```