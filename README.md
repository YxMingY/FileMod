> # 权限数字与字母代表的含义
>>                        作者: xMing
---                      
&nbsp;&nbsp; *使用命令行的操作方式时，我们总是因为一些原因使用chmod这个更改文件权限的指令，比如777权限，755权限之类的，但是他们都代表什么含义呢*
 ### 首先我们了解一下字母的含义
* r 即read，读文件的权限，就是查看文件内容，如cat指令  
* w 即write，更改文件的的权限，包括mv，rm，vi
* x 即execute，执行文件的权限，例如执行一个编译好的c语言文件，直接输入文件路径
 ### 然后我们来看看文件的权限
 &nbsp;&nbsp; *使用[ls -l 文件名]查看一个文件的权限，会显示如下内容*  
   **以777权限为例，一个有777权限的文件应显示**  
      -rwxrwxrwx  
      
   * 开头的第一个字符如果是'-'那就是一个文件，如果是'd'那就是一个文件夹
   * 前面我们知道，rwx指拥有这个文件的所有权限，那为什么会有3个rwx呢
   * 第一个rwx指这个文件的主人的权限;第二个rwx指不是主人，但和主人在同一个权限组的人的权限;第三个rwx指不在其权限组也不是文件主人的普通用户的权限
   * 另: 没有的权限显示为'-'
   * 前面说777权限，一个7就代表一个rwx
 ### 那么其他数字都代表啥呢
*以下是我整理出的数字与字母对照表

| 数字 | 字母 |
| :-: | :-: |
|  0  | --- |
|  1  | --x |
|  2  | -w- |
|  3  | -wx |
|  4  | r-- |
|  5  | r-x |
|  6  | rw- |
|  7  | rwx |
## 就是这样啦  
