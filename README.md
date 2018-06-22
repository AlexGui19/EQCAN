# EQCAN

界面是C#搭建，dbc的解析具体实现是由java写出

C#和java混合编程，

1. 把java打包成jar
2. 利用ikvm把jar生成dll

a.  javac HwJavaClass.java
    jar cvf HwJarName.jar HwJavaClass.class
    ikvmc -out:HwDllname.dll HwJarName.jar
    
    进入CMD，cd到demo.java所在路径：
    先执行：javac   demo.java
    再执行：ikvmc  demo.class

    
b.  Ecplise把javaProject Export成jar
    ikvmc -out:HwDllname.dll HwJarName.jar




新建C#的Form程序，在“解决方案”--“引用”中添加demo.dll和上面所提到的四个IKVM的dll；


IKVM.OpenJDK.ClassLibrary.dll

IKVM.OpenJDK.Core.dll

IKVM.Runtime.dll

IKVM.Runtime.JNI.dll

