---
layout: post
title: 一句话写函数
date: 2019/11/9
categories: blog
tags: [Python,算法]
description: 
---
<P>def trim(s):</P>
<P>if s:</P>
<P>if s[0]==" ":return trim(s[1:])</P>
<P>if s[-1]==' ':return trim(s[:-1])</P>
<P>return s</P>
<P>else:return s</P>
<P>if trim('hello  ') != 'hello':</P>
<P>     print('测试失败!')</P>
<P>elif trim('  hello') != 'hello':</P>
<P>     print('测试失败!')</P>
<P>elif trim('  hello  ') != 'hello':</P>
<P>     print('测试失败!')</P>
<P>elif trim('  hello  world  ') != 'hello  world':</P>
<P>print('测试失败!')</P>
<P>elif trim('') != '':</P>
<P>    print('测试失败!')</P>
<P>elif trim('    ') != '':</P>
<P>    print('测试失败!')</P>
<P>else:</P>
<P>    print('测试成功!')</P>
<P>转载请注明原链接 </P>


   




















