# 添加基本操作

# Magit相关操作

## 查找关于magit的命令

1. 输入 `M-m ?` 然后输入 `magit` 查看查询出来的命令
2. 发现出来的命令都是以 `M-m g` 开头的,所以确定了相关命令

## 使用magit

1. 打开目录中的文件,输入 `M-m g s` 查看stage的文件(已经add的).如果之前没有建立过git仓库,会提示创建仓库.选择 `仓库目录/.` ,`仓库目录/..` 为上级目录
2. 如果没有 `M-m g` 的命令,打开 **.spacemacs** 文件,开启一下git插件即可, 输入 `M-m f e R` 执行设置

## Magit界面中

1. 输入 `?` 表示显示帮助
2. 输入 `q` 表示退到上一个页面
3. 输入 `s` 表示将相应的文件或者所有文件(光标在组上)变为 **stage** (已经add)状态,
4. 输入 `u` 表示变为 **unstage** (没有add)的状态
5. 输入 `cc` 表示对 **stage** 中的进行 `commit` ,在打开的位置中输入注解,输入完之后 `C-c C-c` 进行提交
6. 在页面中输入 `C-t` 可以显示当前页面中可以执行的命令
7. 输入 `Fu/p` 从远程上拉取, **u** 代表主库, **p** 代表其他分支库(如果设置过的话) `Fe` 是自己填写地址
8. 输入 `pu` 推送到服务器. `pe` 选择服务器的分支, `po` 选择自己的分支, `pT` 推送一个标签, `pt` 推送所有的标签
9. 输入 `ll` 查看提交日志(当前分支)
10. 输入 `!s` 在控制台中执行git命令(初次使用需要设置用户名和邮箱)

[magit简介](http://jixiuf.github.io/blog/000100-emacs-magit.html)

# 其他常用操作

1. 关闭当前窗口 `C-x 0`
2. 查询命令 `M-m ?`
3. **SPC** 在这里是指的 `M-m m`
