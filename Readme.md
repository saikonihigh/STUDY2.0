# 9月第 ~~2~~ 3周学习计划

## 	目标

> ![image](https://github.com/saikonihigh/README/blob/master/QQ%E6%8B%BC%E9%9F%B3%E6%88%AA%E5%9B%BE20190915223058.png)
>
> **补充**：1.了解编程的基础知识

## 	计划

​			每天中午12：00至13：00、晚上19：00至21：30学习

​			空闲时间看教程

# GIT学习记录

##    	9/15

> **廖雪峰教程：**https://www.liaoxuefeng.com/wiki/896043488029600/896827951938304

> **>b站傻瓜教程：**https://www.bilibili.com/video/av10475153?from=search&seid=14166050799172925591 (该教程废弃)

1. 初始设置： git config --global user.name "Your Name"

   ​					git config --global user.email "email@example.com" 							注意账号输入错误不会提示

​	2.创建版本库: mkdir learngit		

​					     cd learngit
​						 pwd

​							/XXXXXX/            （**pwd用于显示当前目录**）

​					用 git init将该目录变为仓库（假装这段是有序列表）

​	3.效果

![QQ拼音截图20190915225357](C:\Users\86132\Desktop\QQ拼音截图20190915225357.png)

### 小结

​		廖老师的教程很易懂，但是我学习的效率太低了，总是忘记代码而且不知道代码的意义和使用方法，已经有人学到删除部分了，我得加把劲了。

## 9/16

### 将文件添加到库里

- 添加到仓库：git add+文件名(带后缀)


- 提交到仓库：git commit -m" "     	-m""内是对文件的说明


![QQ拼音截图20190916130333](C:\Users\86132\Desktop\QQ拼音截图20190916130333.png)

- git status：查看仓库状态


- git diff +文件名：查看具体修改情况


- 文件修改后需要重复添加库里的操作

### 版本回退

- git log：查看提交日志


![QQ拼音截图20190916210812](C:\Users\86132\Desktop\QQ拼音截图20190916210812.png)

- git reset --hard head^：退回上一个版本


- git reset --hard +版本号：退回未来的某个版本（用于撤销上面的操作）


![QQ拼音截图20190916211559](C:\Users\86132\Desktop\QQ拼音截图20190916211559.png)

- git reflog：查看记录的每一次命令（可以查找版本号）


#### 工作区和暂存区

![QQ拼音截图20190916215727](C:\Users\86132\Desktop\QQ拼音截图20190916215727.png)

#### 管理修改

- cat+文件名：查看文档内容


- git diff head -- + 文件名：查看文本改动情况![QQ拼音截图20190916222453](C:\Users\86132\Desktop\QQ拼音截图20190916222453.png)


#### 撤销修改

- git checkout -- +文件名：可以撤销对**工作区**的修改，返回到暂存区或者版本库里（优先暂存区）


- git reset head +文件名：可以把**暂存区**的修改撤销并退回到工作区


版本库的撤回参考**版本回退**，如果上传到了远程库，没救

#### 文件删除

使用git rm +文件名然后commit可以从版本库中删除

若误删且没有commit，可以用checkout还原

### 远程库（添加key完成）

#### 添加远程库

搞定，程序员不需要视力

git push origin master即可将最新修改推送到github

## 9/17

### 分支功能

#### 创建与合并

理解该功能的运行原理

用git checkout -b dev 即可创建新的分支，该代码相当于

```
git branch dev
git checkout dev
```

git branch 可查看当前分支，提交同之前一样，再用git checkout master 即可切换到主分支

用git merge dev 能够将master合并到master，命令用于合并指定分支到**当前分支**

完成后输入 git branch -d dev 删除分支

用字符**switch**效果等同于使用checkout（在使用分支功能上）

不需要的**未合并**分支直接用git branch -**D** feature-vulcan强制删除

#### 解决冲突

在两个分支同一文档同一部分**都**进行了修改，在合并时便会冲突

用status可以得知冲突的文件

Git用`<<<<<<<`，`=======`，`>>>>>>>`标记出不同分支的内容

修改后保存即可

#### 分支管理策略

一般情况下会使用fast forward模式合并分支，但是在删除分支后信息便会丢失，禁用该功能（合并时使用 git merge **--no-ff -m** "XXXX" dev）就会生成一个新的commit，便能查看分支信息。

因为新生成了一个commit，所以要使用-m参数（？？）

#### 临时分支

如果要处理其他分支上的任务，git stash将工作区的任务储藏起来，再切换分支处理其他任务，完成后有两种方法恢复，git stash list查看储存内容，有两种恢复方法：

1. git stash apply来恢复，但是内容不删除，git stash drop指令可以删除
2. git stash pop一步到位

# Typora学习记录

##     	9/15

[极简教程][https://www.jianshu.com/p/a6a6a22e9393]

[进阶教程][https://blog.csdn.net/WeiDelight/article/details/81011921]

### 	字体部分

​			斜体：*正*   （ctrl+i）	 italics

​			加粗：**细**   （ctrl+b）   blackbody

​			下划线：<u>上</u>  （ctrl+u）（第一反应是up而不是under= =）

​			删除线：~~1~~    （alt+shift+5）还不如直接打出“~~~~“

​			`	背景填充：`嗯哼？快捷键是什么

### 	插入

- 无序列表：（- + space + enter）

- 有序列表：（数字键 + space + enter）


- 引用：> + space + enter` 或者 `ctrl + shift + q 	**怎么用？？？**


- ctrl + home跳转至文章开头


- ctrl + end 跳转至文章末尾**（？？？为什么用不了这个功能）**


- 选中英文单词/中文：**ctrl + d**或者 **ctrl + shift + left/right**左右进行文本选中 （谜一样的操作）
- 按行选中：ctrl + l

###### 小结

​		初步了解和使用了typora，记住了几个简单的快捷键，一方面熟悉快捷键，另一方面养成习惯，以后尽量使用键盘操作，感觉效率会比使用鼠标要高。

​		顶不住了，还要写通讯稿。

## 9/16

摸了

## 9/17

实践就是最好的记录[^1]

| 因为 | 我   | 真的 | 太难了 |
| ---- | :--- | ---- | ------ |
| 这个 | 功能 | 太   | 好玩了 |

- 无序列表：输入-之后输入空格
- 有序列表：输入数字+“.”之后输入空格

# 备忘录

1. ~~弄明白换行自带序号（1.）的机制~~	这是有序列表功能

2. ~~用 git add +文件时无法识别文件名中的空格的问题~~	这个我还真的不懂.JPG

3. [^1]:其实就是懒啦



