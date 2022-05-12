# Git
[Git命令行操作](#git命令行操作)
[Git图形化界面操作](#git图形化界面操作)
### Git命令行操作
[Git](#git)
1. Git本地库初始化：`git init`
2. 设置签名：
    * 形式：
        * 用户名
        * Email地址
    * 作用：区分不同开发人员的身份
    * 辨析：这里设置的签名和登录远程库（代码托管中心）的账号、密码没有任何关系
    * 命令：
        * 项目级别/仓库级别：仅在当前本地库范围内有效
            * `git config`
            * example:`git config user.name tom_pro`
            `git config user.email Email`
            * 信息保存在`./.git/config`目录下`.git`是一个隐藏目录
        * 系统用户级别：登录当前操作系统的用户范围
            * `git config --global`
            * example:`git config --global user.name tom_glb`
            `git config --global user.email Email`
            * 系统用户信息保存在**家目录**中，使用`~`进入家目录，使用`cat ./.git/config`查看
        * 级别优先级
            * 就近原则：项目级别优先于系统用户级别，二者都有时采用项目级别的签名
            * 如果只有系统用户级别的签名，就医系统用户级别的签名为准
            * 不允许二者都没有
3. 提交操作：
    * `git add filename`
        * `git reset filename`撤回`git add`操作。
        * 如果是修改已经存在的文件，可调过这一步

    * `git commit filename`
        * `git commit -m "modify notion" filename`可以跳过`vim`编辑器阶段
4. 查看历史版本
    * `git log`查看所有提交的版本的所有信息，`HEAD`（链表指针）指向当前版本。多屏显示的控制方式：
        * 空格向下翻页
        * b向上翻页
        * q退出
    * `git log --pretty=oneline`以一行的方式显示（一般IDE的git插件显示记录是非常方便的）
        * ==`git log --oneline`
    * `git reflog`会打印出指针以及每个版本的链表节点的位置

5. 前进后退历史版本的指令及其原理
***~~（这一节没有吃透，需要再看一遍）~~***
    * `git reset --hard hashvalue`
    * `git reset --hard HEAD^`只能一步一步往后查看
    * `git reset --hard HEAD~n`表示后退n步
    * `git help reset`查看reset指令的参数如`--hard --mixed --hard`等
6. 比较文件
    * `git diff filename`默认和缓存区比较
    * `git diff HEAD filename`：当工作区文件添加到缓存区后，可以使用该命令使工作区与本地库比较
7. [分支管理](https://www.runoob.com/git/git-branch.html "runoob:分支管理")
    *在开发过程中不想对master造成污染，就需要使用分支管理，最后使用指令`merge`合并到master*
* 创建分支：`git branch`
* 查看分支：`git branch -v`
* 切换分支：`git checkout branch_name`
* 合并分支：
    * 1.切换到接收修改的分支（合并其它分支，增加新内容）
    * 2.
* 解决冲突：``

### Git图形化界面操作
[Git](#git)
