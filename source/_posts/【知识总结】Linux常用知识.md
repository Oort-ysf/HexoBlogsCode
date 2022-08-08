---
title: 【知识总结】Linux常用知识
date: 2022-08-08 21:37:13
tags: 知识总结
description: Linux常用知识
---

## 1、压缩/解压

### 1.1、压缩

~~~bash
# 将指定文件打包成*.tar
tar –cvf {压缩包名称}.tar {files}
# 将指定文件打包成*.tar.gz
tar –czf {压缩包名称}.tar.gz {files}
# 将指定文件打包成*.tar.bz2
tar –cjf {压缩包名称}.tar.bz2 {files}
# 将指定文件打包成*.tar.Z
tar –cZf {压缩包名称}.tar.Z {files}
# 将指定文件打包成*.rar
rar a {压缩包名称}.rar {files}
# 将指定文件打包成*.zip
zip {压缩包名称}.zip {files}
~~~



### 1.2、解压

~~~bash
# 解压 tar包
tar –xvf {压缩包名称}.tar
# 解压tar.gz
tar -xzvf {压缩包名称}.tar.gz
# 解压 tar.bz2
tar -xjvf {压缩包名称}.tar.bz2
# 解压tar.Z
tar –xZvf {压缩包名称}.tar.Z
#  解压rar
unrar e {压缩包名称}.rar
# 解压zip
unzip {压缩包名称}.zip
~~~



## 2、grep

### 2.1、筛选关键字

~~~bash
cat {file_name} | grep {key_word}
~~~



### 2.2、筛选上下文

~~~bash
# 筛选匹配目标及上下5行
grep -C 5 {key_word} {file_name}

# 筛选匹配目标及前5行
grep -B 5 {key_word} {file_name}

# 筛选匹配目标及后5行
grep -A 5 {key_word} {file_name}
~~~

