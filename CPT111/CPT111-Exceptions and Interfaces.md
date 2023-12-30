CPT111-Exceptions and Interfaces



*: Double.parseDouble()是将括号内的内容变成double类型，如果要变成int，则用

Integer.parselnt()



Case1:  NumberFormatException

```
//Case1 :NumberFormatException
public static void division(){
    Scanner scanner = new Scanner(System.in);
    System.out.println("Please input first value:");
    String in1 = scanner.nextLine();
    //可以注意一下的是在不同的数据类型下，nextXXXX的格式不同
    double d1 = Double.parseDouble(in1);
    System.out.print("Please inout second value:");
    String in2 = scanner.nextLine();
    double d2 = Double.parseDouble(in2);
    System.out.println("The result is :"+d1/d2);
    //当输入的String不是数字时，就会出现编译没错，但没法run的情况。
    //这种数字格式化异常。
}
```

Case2:  ArrayIndexOutOfBounds

```
public static int Findname(String name, String[] names){
    for (int i=0; i<names.length;i++){
        if (name.equals(names[i])){
            return i;
        }
    }
    return -1;
}


public static void main(String[] args) {
    //division();
    String[] names = {"Andrew", "Erick", "Yan"};
    int indice = Findname("Andrew",names);
    System.out.println(indice);
}
```

Case3: NullPointerException

```
//Case3：NullPointerException
private static int findMin(int[] numbers){
    int minSoFar = numbers[0];
    for (int i=0; i<numbers.length;i++){
        if (numbers[i]<minSoFar){
            minSoFar = numbers[i];
        }
    }
    return minSoFar;
}

public static void main(String[] args) {
    findMin(null);
}
```



**Handling Exceptions**

1.) Report the exception and terminate the program

2.) fix the exceptional condition and resume normal execution 

3.) report the exception to a log and resume execution. (not discussed in this module!)

















