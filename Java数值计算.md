## Java数值计算

### BigDecimal

```java
BigDecimal bignum1 = new BigDecimal("10");
		BigDecimal bignum2 = new BigDecimal("5");
		BigDecimal bignum3 = null;
		
		//加法
		bignum3 =  bignum1.add(bignum2); 	 
		System.out.println("和 是：" + bignum3);
		
		//减法
		bignum3 = bignum1.subtract(bignum2);
		System.out.println("差  是：" + bignum3);
		
		//乘法
		bignum3 = bignum1.multiply(bignum2);
		System.out.println("积  是：" + bignum3);
		
		//除法
		bignum3 = bignum1.divide(bignum2);
		System.out.println("商  是：" + bignum3);
```

### 保留小数

```java
//BigDecimal setScale 函数,RoundingMode 舍入模式
System.out.println(BigDecimal.valueOf(1 / 3D).setScale(1, RoundingMode.HALF_UP));
```

### error

####  Exception in thread "main" java.lang.ArithmeticException: Non-terminating decimal expansion; no exact representable decimal result.

出现无限循环小数，指定保留小数限定即可。

```java
BigDecimal.valueOf(between).divide(BigDecimal.valueOf(month * 12), 1, RoundingMode.HALF_UP).toString()
```



### 参考

bigdecimal 加减法：https://blog.csdn.net/limingchuan123456789/article/details/12524495