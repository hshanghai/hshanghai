title: vimBasics
date: 2017-12-09 02:16:16
categories: linux
tags: [vim,linux]
---
## 启动vim
vim file1 file2 file3     一次打开多个文件
:open file 在vim窗口打开一个新文件
:bn 切换下一个文件  :bp 切换上一个文件
:args 查看当前打开的文件列表，当前正在编辑的会用[]括起来
<!--more-->
## 插入命令
i 在当前位置插入
I 在当前位行首插入
a 在当前位置后插入
A 在当前行尾插入
o 在当前行插入下一行
O 在当前行插入上一行
## 查找命令
/text 查找text文本，按n查找下一个N查找上一个
?text 查找text文本，方向查找
:set ignorecase 忽略大小写查找
:set noignorecase 不忽略大小写查找
:set hlsearch 高亮显示查找结果，全部高亮
:set nohlsearch 关闭高亮
:nohlsearch 关闭当前高亮显示，下次查询继续高亮
:set incsearch 逐步查找，对当前键入的字符进行查找而不必等键入完成
:set wrapscan 重新搜索，在搜索到文件头或尾，返回继续查找，默认开启
## 替换命令
ra 将当前字符替换为a 当前字符即光标所在字符
s/old/new/ 用old替换new，替换当前行第一个匹配
s/old/new/g 用old替换new，替换当前行的多有匹配
%s/old/new/ 用old替换new，替换所以行的第一个匹配
%s/old/new/g 用old替换new，替换整个文件的所以匹配
:10,20 s/^/    /g 在第10行到20行每行前面加4个空格，用于缩进
ddp 交换光标所在行和其近邻的一行
## 移动命令
h 左移动一个字符
l 右移动一个字符
k 上移动一个字符
j 下移动一个字符
w 向前移动一个单词，光标在单词首部，会自动跳转下一行
b 向后移动一个单词 2b向前移动2个单词
0或^ 数字0移动到本行第一个字符上
$ 移动到本行尾部
gg 移动到文件头或[[
G 移动到文件尾部或]]
ctrl+e 向下滚动一行
ctrl+y 向上滚动一行
ctrl+d 向下关东半屏
ctrl+u 向上滚动半屏
ctrl+f 向下滚动一屏
ctrl+b 向上滚动一屏
## 撤销和重做
u 撤销
U 撤销对整行的操作
ctrl+r 重做，既撤销的撤销
## 删除命令
x 删除当前字符 3x删除当前3个字符 dl同等左右
X 删除当前字符的前一个字符 dh 同等作用
dd 删除当前行
dj 删除上一行
dk 删除下一行
10d 删除当前行开始的10行
D 删除当前字符至末尾 d$ 同等作用 
kdgg 删除当前行之前的所以行（不包括当前行）
jdG 删除当前之后的所有行（不包含当前行
:1,10d 删除1-10行
:11,$d 删除11行后所有行
:1,$d 删除所有行
J 删除两行之间的空行，实际是合并两行
## 拷贝和粘贴
yy 拷贝当前行  nyy拷贝当前后10行（包括当前行）
p 在当前光标后粘贴，如果之前使用yy命令来复制一行，那么就在当前行下一行复制
shift+p 上一行粘贴
:1,10 co 20 复制1-10行到第20行后面
:1,$ co $ 复制整个文件并粘贴到尾部
ddp 交换当前行与其下一行   也可dd删除当前行，光标移动任意位置p粘贴
xp 交换当前字符和后一个字符

[来源](https://www.cnblogs.com/softwaretesting/archive/2011/07/12/2104435.html)
