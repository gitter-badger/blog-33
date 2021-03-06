---
title: CTF day 01
date: 2022-01-19 22:50:22
updated: 2022-01-19 22:50:22
tags:
- ctf
category: 学习笔记
cover: https://cdn.jsdelivr.net/gh/AkaraChen/GalgamePic@main/20220216230304.png
---

## 1.给一段信息还原明文

```textile
0126 062 0126 0163 0142 0103 0102 0153 0142 062 065 0154 0111 0121 0157 0113 0111 0105 0132 0163 0131 0127 0143 066 0111 0105 0154 0124 0121 060 0116 067 0124 0152 0102 0146 0115 0107 065 0154 0130 062 0116 0150 0142 0154 071 0172 0144 0104 0102 0167 0130 063 0153 0167 0144 0130 060 0113 
```

首先观察这段文字，没有一位大于 7 的数，因此可以得出应该是八进制数，那现在就写 python 把这堆数转换成八进制:

```python
string = "0126 062 0126 0163 0142 0103 0102 0153 0142 062 065 0154 0111 0121 0157 0113 0111 0105 0132 0163 0131 0127 " \
         "0143 066 0111 0105 0154 0124 0121 060 0116 067 0124 0152 0102 0146 0115 0107 065 0154 0130 062 0116 0150 " \
         "0142 0154 071 0172 0144 0104 0102 0167 0130 063 0153 0167 0144 0130 060 0113"
string = string.split(" ")
password = ''
for x in string:
    password += chr(int(x, 8))
print(password)
```

得到这一串字符：

`V2VsbCBkb25lIQoKIEZsYWc6IElTQ0N7TjBfMG5lX2Nhbl9zdDBwX3kwdX0K`

嗯，感觉看着像是 base64，那就改下最后一行代码

```python
print(base64.b64decode(password))
```

得到结果如下

`b'Well done!\n\n Flag: ISCC{N0_0ne_can_st0p_y0u}\n'`

看起来我做的第一道题解出答案了()

## 2.easy_crypto

解压之后只给了一个 txt 文件，内容如下

0010 0100 01 110 1111011 11 11111 010 000 0 001101 1010 111 100 0 001101 01111 000 001101 00 10 1 0 010 0 000 1 01111 10 11110 101011 1111101

第一反应是二进制，跟上道题一样这么硬解

```python
string = "0010 0100 01 110 1111011 11 11111 010 000 0 001101 1010 111 100 0 001101 01111 000 001101 00 10 1 0 010 0 " \
         "000 1 01111 10 11110 101011 1111101"
string = string.split(" ")
flag = ''
for x in string:
    flag += chr(int(x, 2))
print(flag)
```

输出如下:

`{ 
  +}`

解出来俩大括号，完蛋，然后看 bugku 下面的提示，是摩斯电码，于是修改如下

```python
string = "0010 0100 01 110 1111011 11 11111 010 000 0 001101 1010 111 100 0 001101 01111 000 001101 00 10 1 0 010 0 " \
         "000 1 01111 10 11110 101011 1111101"
string = string.replace("0", ".")
string = string.replace("1", "-")
string = string.split(" ")
morse = ""
for x in string:
    morse += x + " "
print(morse)
```

输出结果是这样的：

`..-. .-.. .- --. ----.-- -- ----- .-. ... . ..--.- -.-. --- -.. . ..--.- .---- ... ..--.- .. -. - . .-. . ... - .---- -. ----. -.-.-- -----.-`

然后去摩斯电码解密试一下

结果如下

`flag%u7bm0rse_code_1s_interest1n9!%u7d`

然后吧 `u7b` 和 `u7d` 换成 `{}` ，就这么解出来了()

## 3. 进制转换

很简单，但就是不会写脚本实现，python 快忘干净了，自带那些包一个都不记得

来，基础知识，d 代表十进制，b 代表二进制，x 十六进制，o 代表 8 进制。

这题提供了这个字符串

```python
string = 'd87 x65 x6c x63 o157 d109 o145 b100000 d116 b1101111 o40 x6b b1100101 b1101100 o141 d105 x62 d101 b1101001 ' \
         'd46 o40 d71 x69 d118 x65 x20 b1111001 o157 b1110101 d32 o141 d32 d102 o154 x61 x67 b100000 o141 d115 ' \
         'b100000 b1100001 d32 x67 o151 x66 d116 b101110 b100000 d32 d102 d108 d97 o147 d123 x31 b1100101 b110100 d98 ' \
         'd102 b111000 d49 b1100001 d54 b110011 x39 o64 o144 o145 d53 x61 b1100010 b1100011 o60 d48 o65 b1100001 x63 ' \
         'b110110 d101 o63 b111001 d97 d51 o70 d55 b1100010 d125 x20 b101110 x20 b1001000 d97 d118 o145 x20 d97 o40 ' \
         'd103 d111 d111 x64 d32 o164 b1101001 x6d o145 x7e'
```

好的，直接 spilit，转十六进制，最后 hex 转字符串，完事

```python
import binascii

string = 'd87 x65 x6c x63 o157 d109 o145 b100000 d116 b1101111 o40 x6b b1100101 b1101100 o141 d105 x62 d101 b1101001 ' \
         'd46 o40 d71 x69 d118 x65 x20 b1111001 o157 b1110101 d32 o141 d32 d102 o154 x61 x67 b100000 o141 d115 ' \
         'b100000 b1100001 d32 x67 o151 x66 d116 b101110 b100000 d32 d102 d108 d97 o147 d123 x31 b1100101 b110100 d98 ' \
         'd102 b111000 d49 b1100001 d54 b110011 x39 o64 o144 o145 d53 x61 b1100010 b1100011 o60 d48 o65 b1100001 x63 ' \
         'b110110 d101 o63 b111001 d97 d51 o70 d55 b1100010 d125 x20 b101110 x20 b1001000 d97 d118 o145 x20 d97 o40 ' \
         'd103 d111 d111 x64 d32 o164 b1101001 x6d o145 x7e'
string = string.split(" ")
flag = ''
for x in string:
    if x[:1] == 'd':
        text = str(hex(int(x[1:], 10)))
    elif x[:1] == 'b':
        text = str(hex(int(x[1:], 2)))
    elif x[:1] == 'x':
        text = str(hex(int(x[1:], 16)))
    else:
        text = str(hex(int(x[1:], 8)))
    flag += binascii.unhexlify(text.replace('0x', '')).decode()
print(flag)
```

## 4.ASIII

这都什么神仙题...

```python
string = 'ab979adf8e8a969c94df9d8d908891df999087df958a928fdf90899a8ddf8b979adf939e8586df9b9098dedfab979adf9993' \
         '9e98df968cc5df9d9b9c8b9984a6cf8aa09e8d9aa08c929e8dc882'
```

给这么个字符串，一眼十六进制，不过需要我们手动切片

```python
str_list = []
while len(string) > 0:
    str_list.append(string[:2])
    string = string[2:]
```

然后，把十六进制转成十进制

`171 151 154 223 142 138 150 156 148 223 157 141 144 136 145 223 153 144 135 223 149 138 146 143 223 144 137 154 141 223 139 151 154 223 147 158 133 134 223 155 144 152 222 223 171 151 154 223 153 147 158 152 223 150 140 197 223 157 155 156 139 153 132 166 207 138 160 158 141 154 160 140 146 158 141 200 130`

大部分数都是大于 126 的，所以不能直接用作 asiii 码，根据网上的大佬推断，应该用 256-求出来的值，然后转 asiii，嗯，这思路，无懈可击，大概吧。。。

```python
flag = ''
for x in str_list:
    flag += chr(255 - int(x, 16))
print(flag)
```

奶奶的，你玩阴的是吧

![](https://pic.rmb.bdstatic.com/bjh/9a93e383053dc57966334de093f1080a.png)

## 奇怪的密码

```python
string = 'gndk€rlqhmtkwwp}z'
i = 0
while i < len(string):
    print(chr(ord(string[i]) - (i + 1)), end="")
    i += 1
```

flag 和 gndk 的 asiii 码刚好各偏离 [1,2,3,4] ，所以后面同理，最后全整完，输出 `flag₧lei_ci_jiami` ，更改成 `flag{lei_ci_jiami}` 对了