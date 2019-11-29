# procs-convert.md
⊕ [Mac下GBK与UTF8编码文件的批量转换 - 思考的智慧，知识源于思考 - CSDN博客](https://blog.csdn.net/tianxiawuzhei/article/details/48711633)

## start
```sh
# 显示可识别的编码名称
iconv --list
iconv -f GB2312 -t UTF-8 a.html > b.html # 转换GB2312编码的文件a.html为UTF-8编码，存入b.html
iconv -f GB2312 -t BIG5 a.html > b.html # 转换GB2312编码的文件a.html为BIG5编码，存入b.html

find *.py -exec sh -c "iconv -f GB18030 -t UTF8 {} > {}.py" \;  
# 上面命令中的GB18030，如果你转换前的编码为GB2312，将 GB18030 代替为 GB2312 即可。
```
