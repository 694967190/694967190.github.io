---
layout: post
title: 一句话写函数
date: 2019/11/9
categories: blog
tags: [Python,算法]
description: 
---

def trim(s):
    if s:
        if s[0]==" ":return trim(s[1:])
        if s[-1]==' ':return trim(s[:-1])
        return s
    else:return s
if trim('hello  ') != 'hello':
    print('测试失败!')
elif trim('  hello') != 'hello':
    print('测试失败!')
elif trim('  hello  ') != 'hello':
    print('测试失败!')
elif trim('  hello  world  ') != 'hello  world':
    print('测试失败!')
elif trim('') != '':
    print('测试失败!')
elif trim('    ') != '':
    print('测试失败!')
else:
    print('测试成功!')

转载请注明原链接 












