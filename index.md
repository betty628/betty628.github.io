pwn的学习

001
https://blog.csdn.net/2401_87716819/article/details/145141756?spm=1001.2014.3001.5501
002
https://blog.csdn.net/2401_87716819/article/details/145214971?spm=1001.2014.3001.5501
003：kail突然打不开了，今天就写了一道crypto的题
题目：

[LitCTF 2023]md5的破解

原题解析：

from Crypto.Util.number import *
from hashlib import md5
from secret import flag
 
#flag全是由小写字母及数字组成
m=md5(flag).hexdigest()
print(flag[:13]+flag[15:18]+flag[19:34]+flag[35:38])
print(m)
# b'LitCTF{md5can3derypt213thoughcrsh}'
#496603d6953a15846cd7cc476f146771
 
思路：遍历小写字母及数字，将最终组成的内容（先转为字节型数据，接着计算md5值最后转换16进制）与499.........71作比较

import string
import hashlib
all = '0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ-_}{'
for a in all:
for b in all:
for c in all:
for d in all:
s = 'LitCTF{md5can'+a+b+'3de'+c+'rypt213thoughcr'+d+'sh}'
print(s)
if hashlib.md5(s.encode('utf-8')).hexdigest() == '496603d6953a15846cd7cc476f146771':
print("Find it: "+s)
exit(0)
结果：LitCTF{md5can123dexrypt213thoughcrpsh}

