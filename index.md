pwn的学习

#001
(https://blog.csdn.net/2401_87716819/article/details/145141756?spm=1001.2014.3001.5501)

#002
(https://blog.csdn.net/2401_87716819/article/details/145214971?spm=1001.2014.3001.5501)

#003：kail突然打不开了，今天就写了一道crypto的题
-题目：

-[LitCTF 2023]md5的破解

-原题解析：

![图片](https://github.com/user-attachments/assets/91f2df72-c027-49f8-acce-af8b9e758b03)

 
思路：遍历小写字母及数字，将最终组成的内容（先转为字节型数据，接着计算md5值最后转换16进制）与499.........71作比较
![图片](https://github.com/user-attachments/assets/d16c12fd-1f55-4176-b4a8-b7342394a21a)


结果：LitCTF{md5can123dexrypt213thoughcrpsh}

