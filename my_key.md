# 自定义快捷键说明

```
常用快捷键
H 行首
L 行尾
,n 展示菜单

,p  打开ctrlp搜索
,f 查看最近打开文件；ctrl+x , ctrl+v 分屏打开；回车当前打开

ctrl + j/k 进行上下移动
ctrl + x/v 分屏打开该文件 [重要**]
ctrl + t   在新tab中打开该文件

:ls buff列表

v 选择
,v 区域大块选择

ctrl+n 相对行号/绝对行号
,sa 全选

,空格    去掉当前行末尾空格

--------------
ci'、ci"、ci(、ci[、ci{、ci< - 分别更改这些配对标点符号中的文本内容
di'、di"、di(或dib、di[、di{或diB、di< - 分别删除这些配对标点符号中的文本内容
yi'、yi"、yi(、yi[、yi{、yi< - 分别复制这些配对标点符号中的文本内容
vi'、vi"、vi(、vi[、vi{、vi< - 分别选中这些配对标点符号中的文本内容>}])>}])>}])>}])
--------------

--------------
,, + w  跳转
,, + fe  查找'e',快速跳转定位到某个字符位置
,,j      快速决定移动到下面哪行(比用行号/j移动快)
,,k      快速移动到上面哪行
--------------

--------------
F2 隐藏行号 :no nu
F5 粘贴模式 PASTE
F9 tabar 函数列表展示
--------------

--------------
格式化对齐
选中模式下；输入ga; 然后命令号输入 对齐指令
=        首个=号对齐,文字左对齐
*=       所有=号对齐,文字右对齐
**=
--------------

--------------
 环绕符号(ys=you surround)
ds' 删除单词周围'
cs"' 替换单词两侧" 为'

 cs"'       ("Hello world!" -> 'Hello world!'
 ds"        ("Hello world!" -> Hello world! )
 ysiw"      (Hello -> "Hello")
 yss"       (Hello world -> "Hello world")
--------------
```




以下快捷键中==
```
F1   关掉，防止跳出帮助
F2  set nu/nonu
F3  set list/nolist
F4  set wrap/nowrap
F5  set paste/nopaste
F6  syntax on/off
F9 tagbar
F10 运行当前文件(quickrun)

,n

#       正向查找光标下的词
*       反向查找光标下的词

8. buffer操作(不建议, 建议使用ctrlspace插件来操作)
[b    前一个buffer
]b    后一个buffer
<-    前一个buffer
->    后一个buffer

9. 按键修改
Y         =y$   复制到行尾
U         =Ctrl-r
,sa       select all,全选
,v        选中段落


空格 /开启查找
Y   =y$   复制到行尾
w!!  以sudo的权限保存
,sa   全选(select all)
hjkl  上下左右，强迫使用，要解开的自己改
ctrl + jkhl 进行上下左右窗口跳转,不需要ctrl+w+jkhl

,tn  new tab
,tc  tab close
,to  tab only
,tm  tab move
,te  new tab edit
ctrl+n  相对行号绝对行号变换，
        默认用相对行号 http://jeffkreeftmeijer.com/2012/relative-line-numbers-in-vim-for-super-fast-movement/
5j/5k  在相对行号模式下，往上移动5行 往下移动5行，不喜欢注解line 142附近relativenumber配置

,p 开启文件搜索 ctrlp
,f 开启最近打开文件查找
,/ 去除匹配高亮
```


```
1.快速注释 scrooloose/nerdcommenter
[d] shift+v+方向键选中(默认当前行)
-> ,cc      加上注释
-> ,cu      解开注释
-> ,c<space> 加上/解开注释
-> ,cy      先复制再注解, p可以粘贴未注释前的代码
```

```
2.快速编辑 tpope/vim-surround +tpope/vim-repeat
必装，很给力的功能，快速给词加环绕符号,例如引号, 注意(括号, 左括号会加空格, 右括号不会)
repeat进行增强,'.'可以重复使用命令 (ys=you surround)

    cs"'
    "Hello world!" -> 'Hello world!'

    ds"
    "Hello world!" -> Hello world!

    ysiw"
    Hello -> "Hello"

    yss"
    Hello world -> "Hello world"

    cst"
    <a>abc</a>  -> "abc"

    veeS"
    hello world -> "hello world"

    ys$" 当前到行尾, 引号引住"
```

```
3.去行尾空格 bronson/vim-trailing-whitespace
将代码行最后无效的空格标红
,空格    去掉当前行末尾空格
```

```
4.位置跳转Lokaltog/vim-easymotion 必装，效率提升杀手锏，跳转到光标后任意位置
配置(我的leader键配置 let g:mapleader = ',')
,, + w  跳转
,, + fe  查找'e',快速跳转定位到某个字符位置
,,j      快速决定移动到下面哪行(比用行号/j移动快)
,,k      快速移动到上面哪行
,,l      本行, 向后快速移动
,,h      本行, 向前快速移动
,,.      重复上一次easymotion命令
```

```
区块伸缩 terryma/vim-expand-region 视图模式下可伸缩选中部分，用于快速选中某些块
v 增加选中范围
V 减少选中范围
```

```
.mark跳转 kshenoy/vim-signature 必装, 快速打标签, 随时跳回标签位置
m[a-zA-Z]   打标签
'[a-zA-Z]   跳转到标签位置
'. 最后一次变更的地方
'' 跳回来的地方

m<space>    去除所有标签
```

```
插件: 当前文件快速函数搜索:tacahiroy/ctrlp-funky
解决问题:使用tagbar当函数比较多的时候,移动耗时较长,使用快速搜索快很多
,fu   进入当前文件函数搜索
,fU   搜索光标下单词对应函数
```


快速导航

```
目录树 scrooloose/nerdtree
,n  打开 关闭树形目录结构

在nerdtree窗口常用操作：(小写当前，大写root)
x.......收起当前目录树
X.......递归收起当前目录树
r.......刷新当前目录
R.......刷新根目录树

p.......跳到当前节点的父节点
P.......跳到root节点
k/j.....上下移动
K.......到同目录第一个节点
J.......最后一个节点

o.......Open files, directories and bookmarks

s.......split上下分屏[原来是i, 改键]
v.......vsplit左右分屏[原来是s, 改键]

c.......将当前目录设为根节点
q.......关闭
```
