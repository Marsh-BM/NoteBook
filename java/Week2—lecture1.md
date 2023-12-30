Week2—lecture1

Square root of a variable:

```
int num1 = 5;
double root = Math.sqrt(num1);
System.out.println(root);
```



Get the maxinum of 2 numbers:

```
 int num2 = 4;
 double r = Math.max(num1,num2);
 System.out.println(r);
```

![](C:\Users\白木-泽\Desktop\屏幕截图 2021-09-15 121034.png)

Triangles-Hypotenuse

![](C:\Users\白木-泽\Desktop\屏幕截图 2021-09-15 122851.png)

```
//勾股定理
double a = 4;
double b = 2;
double c = Math.sqrt(Math.pow(a,2) + Math.pow(b,2));
System.out.println("Value of C " + c);

double d=Math.pow(a,3);
System.out.println(d);
```

```
//勾股定理的另一种方法
double a1 = 4;
double b1 = 2;
double simpleC = Math.hypot(a1, b1);
System.out.println("Simpler Value of C " + simpleC);
```

Triangles-Angles

![](C:\Users\白木-泽\Desktop\屏幕截图 2021-09-15 123944.png)

toDrgree(x):角度转弧度。

toRadians（x）：弧度转角度。

