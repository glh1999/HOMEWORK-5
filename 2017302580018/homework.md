# 网络及分布式计算第五次作业

#### 2017302580018  刘佳媚

---

### 用python实现UDP的16位校验和

源码见UDPCheck.py

验证结果如下，与3.3.2节的计算结果一致。

![image](images\result.png)



------



### 1、P3

##### ![image](images\P3.png)

  解：

​            01010011   

​     +     01100110 

​     ———————

​     =     10111001 

​     +     01110100 

​     ———————

​             00101110

反码为 11010001。

UDP使用该和的反码是因为这样不依赖系统是大端还是小端，而且计算检验和比较简单快速。

接收方检验差错的方法是将三个字节与检验和相加，得到的和为1111111111111111，如果任何一个位为 0，说明出错。

1比特的差错能检测出来，2比特的差错可能会检测不出。

   

---

### 2、P4

##### ![image](images\P4.png) 

  解：

​       a、

​            01011100  

​     +     01100101

​     ———————

​     =     11000001        反码为：00111110。



​     b、

​            11011010  

​     +     01100101

​     ———————

​     =     01000000      反码为： 10111111。



​    c、两个字节变为 01011101、01100100。

  



