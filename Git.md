# Git
[Git命令行操作](#git命令行操作)
[Git图形化界面操作](#git图形化界面操作)
### Git命令行操作
[Git](#git)
1. Git本地库初始化：`git init`
2. 设置签名：
    * 形式：
        * 有户名
        * Email地址
    * 作用：区分不同开发人员的身份
    * 辨析：这里设置的签名和登录远程库（代码托管中心）的账号、密码没有任何关系
    * 命令：
        * 项目级别/仓库级别：仅在当前本地库范围内有效
            * `git config`
            * example:`git config user.name tom_pro`
            `git config user.email Email`
            * 信息保存在`./.git/config`目录下
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
    * `git commit filename`

### Git图形化界面操作
[Git](#git)
