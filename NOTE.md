## Github
# 关键字查询
 awesome，去此标签类型中查询项目<br>
 python tutorial,查询资料，书籍，文档<br>
 socket sample,查询对应技术的代码样本<br>
# Github三要素
## Repository 仓库
 仓库是github项目管理存储基本单位<br>
 一个仓库中存储一个项目，一个用户可以有多个仓库，一般仓库分为public，private
## Commit 提交
 程序员在整个开发周期，有大量的代码资源的迭代和修改，都可以通过commit的方式进行记录，便于程序员回溯代码，即使这些代码被删除<br>
 提交便于使用者观察整个工程的开发流程以及设计流程
## Branch分支
 在仓库中可以有多个分支，分支是代码文件的第一存储单位，默认的仓库主分支为master/main<br>
 分支不仅可以管理代码存储，也便于多人协作开发<br>

## 仓库内容
1. Code,资源存储，代码资源，二进制，项目管理脚本，许可证等等
2. issues，使用时遇到的bug或进行提交，等待反馈
3. README，使用markdown语言编写，工程自述文件，开发进度，版本更新，使用介绍等等
4. LICENSE 许可证
   1. GPL2.0 3.0 Apahce 2.0，Mit，这些许可证给使用者最大使用权限以及最少得限制
## Git软件，分布式版本控制系统
**仓库管理软件，使用git管理私人代码或者企业代码**<br>
本地的是新版，发布的是旧的版本
## 设备认证
### 1.如何让网站的账户也设备进行绑定，后续完成代码的管理以及上传下载
1. git init    //创建本地仓库<br>
2. git config --list   //查看git的配置文件<br>
3. git config --global user.email "邮箱"<br>
4. git config --global user.name "用户名"<br>
5. ssh-keygen -t rsa -C "注册邮箱"  //创建本地密文<br>
6. 去对应的目录找密文文件<br>
7. rsa.pub 复制密文，粘贴 setting->SSH key and GPG-> new ssh key ->粘贴<br>
8. ssh -T git@github.com  //测试关联是否成功<br>

### 2.为目标仓库起别名，定位目标仓库，后续上传
git remote add origin "ssh地址" //为ssh仓库地址创建别名为origin<br>
git remote remove origin //删除origin别名<br>
git remote add origin "ssh地址" //为ssh仓库地址创建别名为origin<br>

## 本地设备与云端仓库的交互逻辑
本地文件通过git add 命令进入git缓冲区，再通过git commit "提交说明"到达本地仓库，再通过git push origin master命令到达云端仓库。<br>
*如果上传的本地分支与云端默认分支一致，则合并分支,不一致则创建新分支*<br>
git add //添加内容<br>
git rm  //删除本地文件并删除仓库数据<br>
git restore  //回复被删除的内容，前提是仓库没有被删除<br>
## 代码更新的依赖关系被破坏
本地内容要比云端新，完成更新替换，但是如果直接修改云端内容，导致本地内容无法再次提交<br>
解决方法：先拉取 git pull 云端内容，与本地内容合并或操作，而后再次pull<br>
git pull --rebase origin master<br>
git rebase --skip //忽略本地内容，保留云端内容<br>
git rebase --abort<br>
git rebase --continue <br>
## 下载开源代码
git clone "https仓库地址"  //下载开源项目的code资源

设置行号： :set nu

Markdown ,文本修饰语言，用特殊符号修饰正文效果<br>

## 标题修饰符\#
# 标题修饰符(一级标题)
## (二级标题)
### (三级标题)
#### (四级标题)
##### (五级标题)

## 正文内容

        输入正文内容，但是如果需要换行，用\<br\>标签

## 修饰正文

   *一段测试文本*

   **一段测试文本**

   ***一段测试文本***

   ~~一段测试文本~~

   这是一段测试文本，将`关键字`凸显出来
## 分割线
 用\-\-\- 表示分割线

---

## 引用效果\>表示
> 一级引用
>> 二级引用
>>> 三级引用
>>>> 四级引用

## 列表修饰符
### 无序列表 \*
* 二次元游戏
  * 原神
    * 克洛琳德
* 战略类
  * 率土之滨
### 有序列表 1.
1. 物理学
   1. 粒子物理
   2. 原子核物理
2. 计算机科学
   1. 分布式架构
   2. 云计算
### 混合列表
1. 测试一级
   * 测试二级
    2. 测试三级

### 表格
名称|技能|排行
--|:--:|--:
雷神|浮生一梦|1
凌华|神里流霜灭|2

### 代码片段
```c
      #include<stdio.h>
      int main{
      printf("hh\n");
      return 0;
      }
```
```cpp
        #incldue<iostream>
```

```python
         import <os>
```

```bash
        echo "测试"
        pwd
        ps aux
        ls -l
```

### 超链接技术
[Github](https://github.com "点击访问")

### 插入图片
![壁纸截图](C://Users//35157//Desktop//1.png "悬停标题")

