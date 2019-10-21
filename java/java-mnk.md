---
title: "Java Mnk"
date: 2019-10-21T20:08:07+08:00
draft: true
---

学习java最少必要知识

Java是由Sun Microsystems公司于1995年5月推出的一种跨平台的，面向对象的通用编程语言。

随着Java的发展，SUN给Java又分出了三个不同版本：  
Java SE：Standard Edition  
Java EE：Enterprise Edition  
Java ME：Micro Edition  
简单来说，Java SE就是标准版，包含标准的JVM和标准库，而Java EE是企业版，它只是在Java SE的基础上加上了大量的API和库，以便方便开发Web应用、数据库、消息服务等，Java EE的应用使用的虚拟机和Java SE完全相同。  
Java ME就和Java SE不同，它是一个针对嵌入式设备的“瘦身版”，Java SE的标准库无法在Java ME上使用，Java ME的虚拟机也是“瘦身版”。  
毫无疑问，Java SE是整个Java平台的核心，而Java EE是进一步学习Web应用所必须的。我们熟悉的Spring等框架都是Java EE开源生态系统的一部分。不幸的是，Java ME从来没有真正流行起来，反而是Android开发成为了移动平台的标准之一，因此，没有特殊需求，不建议学习Java ME。  
  
JDK：Java Development Kit  
JRE：Java Runtime Environment  
简单地说，JRE就是运行Java字节码的虚拟机。但是，如果只有Java源码，要编译成Java字节码，就需要JDK，因为JDK除了包含JRE，还提供了编译器、调试器等开发工具。  
  
JSR规范：Java Specification Request  
JCP组织：Java Community Process  
为了保证Java语言的规范性，SUN公司搞了一个JSR规范，凡是想给Java平台加一个功能，比如说访问数据库的功能，大家要先创建一个JSR规范，定义好接口，这样，各个数据库厂商都按照规范写出Java驱动程序，开发者就不用担心自己写的数据库代码在MySQL上能跑，却不能跑在PostgreSQL上。  
  
Java基础语法  
一个 Java程序可以认为是一系列对象的集合，而这些对象通过调用彼此的方法来协同工作。下面简要介绍下类、对象、方法和实例变量的概念。  
对象：对象是类的一个实例，有状态和行为。例如，一条狗是一个对象，它的状态有：颜色、名字、品种；行为有：摇尾巴、叫、吃等。  
类：类是一个模板，它描述一类对象的行为和状态。  
方法：方法就是行为，一个类可以有很多方法。逻辑运算、数据修改以及所有动作都是在方法中完成的。  
实例变量：每个对象都有独特的实例变量，对象的状态由这些实例变量的值决定。  
  
大小写敏感：Java是大小写敏感的，这就意味着标识符 Hello 与 hello 是不同的。  
类名：对于所有的类来说，类名的首字母应该大写。如果类名由若干单词组成，那么每个单词的首字母应该大写，例如 MyFirstJavaClass 。  
方法名：所有的方法名都应该以小写字母开头。如果方法名含有若干单词，则后面的每个单词首字母大写。  
源文件名：源文件名必须和类名相同。当保存文件的时候，你应该使用类名作为文件名保存（切记 Java 是大小写敏感的），文件名的后缀为 .java。（如果文件名和类名不相同则会导致编译错误）。  
主方法入口：所有的 Java 程序由 public static void main(String []args) 方法开始执行。  
  
Java标识符  
所有的标识符都应该以字母（A-Z 或者 a-z）,美元符（$）、或者下划线（_）开始  
首字符之后可以是字母（A-Z 或者 a-z）,美元符（$）、下划线（_）或数字的任何字符组合  
关键字不能用作标识符  
标识符是大小写敏感的  
合法标识符举例：age、$salary、_value、__1_value  
非法标识符举例：123abc、-salary  
  
Java修饰符  
访问控制修饰符 : default, public , protected, private  
非访问控制修饰符 : final, abstract, static, synchronized  
  
Java数组  
数组是储存在堆上的对象，可以保存多个同类型变量。  
  
Java枚举  
枚举限制变量只能是预先设定好的值。使用枚举可以减少代码中的 bug。  
  
Java 关键字  
访问控制:  
private		私有的  
protected	受保护的  
public		公共的  
类、方法和变量修饰符:  
abstract	声明抽象  
class		类  
extends		扩充,继承  
final		最终值,不可改变的  
implements	实现（接口）  
interface	接口  
native		本地，原生方法（非 Java 实现）  
new			新,创建  
static		静态  
strictfp	严格,精准  
synchronized	线程,同步  
transient	短暂  
volatile	易失  
程序控制语句:  
break		跳出循环  
case		定义一个值以供 switch 选择  
continue	继续  
default		默认  
do			运行  
else		否则  
for			循环  
if			如果  
instanceof	实例  
return		返回  
switch		根据值选择执行  
while		循环  
错误处理:  
assert		断言表达式是否为真  
catch		捕捉异常  
finally		有没有异常都执行  
throw		抛出一个异常对象  
throws		声明一个异常可能被抛出  
try			捕获异常  
包相关:  
import		引入  
package		包  
基本类型:  
boolean		布尔型  
byte		字节型  
char		字符型  
double		双精度浮点  
float		单精度浮点  
int			整型  
long		长整型  
short		短整型  
变量引用:  
super		父类,超类  
this		本类  
void		无返回值  
保留关键字:  
goto		是关键字，但不能使用  
const		是关键字，但不能使用  
null		空  
  
Java注释  
Java支持单行以及多行注释。注释中的字符将被 Java 编译器忽略。  
// 这是单行注释的示例  
/* 这个也是单行注释的示例 */  
/* 这是第一个Java程序  
    *它将打印Hello World  
    * 这是一个多行注释的示例  
    */  
  
Java空行  
空白行或者有注释的行，Java 编译器都会忽略掉。  
  
继承  
在 Java 中，一个类可以由其他类派生。如果你要创建一个类，而且已经存在一个类具有你所需要的属性或方法，那么你可以将新创建的类继承该类。  
利用继承的方法，可以重用已存在类的方法和属性，而不用重写这些代码。被继承的类称为超类（super class），派生类称为子类（subclass）。  
  
接口  
在 Java 中，接口可理解为对象间相互通信的协议。接口在继承中扮演着很重要的角色。  
接口只定义派生要用到的方法，但是方法的具体实现完全取决于派生类。  
  
Java 对象和类  
Java作为一种面向对象语言。支持以下基本概念：  
多态,继承,封装,抽象,类,对象,实例,方法,重载  
对象：对象是类的一个实例（对象不是找个女朋友），有状态和行为。例如，一条狗是一个对象，它的状态有：颜色、名字、品种；行为有：摇尾巴、叫、吃等。  
类：类是一个模板，它描述一类对象的行为和状态。  
男孩（boy）、女孩（girl）为类（class），而具体的每个人为该类的对象（object）。  
  
一个类可以包含以下类型变量：  
局部变量：在方法、构造方法或者语句块中定义的变量被称为局部变量。变量声明和初始化都是在方法中，方法结束后，变量就会自动销毁。  
成员变量：成员变量是定义在类中，方法体之外的变量。这种变量在创建对象的时候实例化。成员变量可以被类中方法、构造方法和特定类的语句块访问。  
类变量：类变量也声明在类中，方法体之外，但必须声明为static类型。  
  
构造方法  
每个类都有构造方法。如果没有显式地为类定义构造方法，Java编译器将会为该类提供一个默认构造方法。  
在创建一个对象的时候，至少要调用一个构造方法。构造方法的名称必须与类同名，一个类可以有多个构造方法。  
  
创建对象  
对象是根据类创建的。在Java中，使用关键字new来创建一个新的对象。创建对象需要以下三步：  
声明：声明一个对象，包括对象名称和对象类型。  
实例化：使用关键字new来创建一个对象。  
初始化：使用new创建对象时，会调用构造方法初始化对象。  
```  
public class Puppy{  
   public Puppy(String name){  
      //这个构造器仅有一个参数：name  
      System.out.println("小狗的名字是 : " + name );  
   }  
   public static void main(String[] args){  
      // 下面的语句将创建一个Puppy对象  
      Puppy myPuppy = new Puppy( "tommy" );  
   }  
}  
```  
  
访问实例变量和方法  
通过已创建的对象来访问成员变量和成员方法，如下所示：  
```  
/* 实例化对象 */  
Object referenceVariable = new Constructor();  
/* 访问类中的变量 */  
referenceVariable.variableName;  
/* 访问类中的方法 */  
referenceVariable.methodName();  
```  
  
源文件声明规则  
一个源文件中只能有一个public类  
一个源文件可以有多个非public类  
源文件的名称应该和public类的类名保持一致。例如：源文件中public类的类名是Employee，那么源文件应该命名为Employee.java。  
如果一个类定义在某个包中，那么package语句应该在源文件的首行。  
如果源文件包含import语句，那么应该放在package语句和类定义之间。如果没有package语句，那么import语句应该在源文件中最前面。  
import语句和package语句对源文件中定义的所有类都有效。在同一源文件中，不能给不同的类不同的包声明。  
  
Java包  
包主要用来对类和接口进行分类。当开发Java程序时，可能编写成百上千的类，因此很有必要对类和接口进行分类。  
Import语句  
在Java中，如果给出一个完整的限定名，包括包名、类名，那么Java编译器就可以很容易地定位到源代码或者类。Import语句就是用来提供一个合理的路径，使得编译器可以找到某个类。  
例如，下面的命令行将会命令编译器载入java_installation/java/io路径下的所有类  
import java.io.*;  
  
Java 基本数据类型  
变量就是申请内存来存储值。也就是说，当创建变量的时候，需要在内存中申请空间。  
内存管理系统根据变量的类型为变量分配存储空间，分配的空间只能用来储存该类型数据。  
  
Java 的两大数据类型:  
内置数据类型  
引用数据类型  
  
内置数据类型  
Java语言提供了八种基本类型。六种数字类型（四个整数型，两个浮点型），一种字符类型，还有一种布尔型。  
byte：  
byte 数据类型是8位、有符号的，以二进制补码表示的整数；  
最小值是 -128（-2^7）；  
最大值是 127（2^7-1）；  
默认值是 0；  
byte 类型用在大型数组中节约空间，主要代替整数，因为 byte 变量占用的空间只有 int 类型的四分之一；  
例子：byte a = 100，byte b = -50。  
short：  
short 数据类型是 16 位、有符号的以二进制补码表示的整数  
最小值是 -32768（-2^15）；  
最大值是 32767（2^15 - 1）；  
Short 数据类型也可以像 byte 那样节省空间。一个short变量是int型变量所占空间的二分之一；  
默认值是 0；  
例子：short s = 1000，short r = -20000。  
int：  
int 数据类型是32位、有符号的以二进制补码表示的整数；  
最小值是 -2,147,483,648（-2^31）；  
最大值是 2,147,483,647（2^31 - 1）；  
一般地整型变量默认为 int 类型；  
默认值是 0 ；  
例子：int a = 100000, int b = -200000。  
long：  
long 数据类型是 64 位、有符号的以二进制补码表示的整数；  
最小值是 -9,223,372,036,854,775,808（-2^63）；  
最大值是 9,223,372,036,854,775,807（2^63 -1）；  
这种类型主要使用在需要比较大整数的系统上；  
默认值是 0L；  
例子： long a = 100000L，Long b = -200000L。  
"L"理论上不分大小写，但是若写成"l"容易与数字"1"混淆，不容易分辩。所以最好大写。  
float：  
float 数据类型是单精度、32位、符合IEEE 754标准的浮点数；  
float 在储存大型浮点数组的时候可节省内存空间；  
默认值是 0.0f；  
浮点数不能用来表示精确的值，如货币；  
例子：float f1 = 234.5f。  
double：  
double 数据类型是双精度、64 位、符合IEEE 754标准的浮点数；  
浮点数的默认类型为double类型；  
double类型同样不能表示精确的值，如货币；  
默认值是 0.0d；  
例子：double d1 = 123.4。  
boolean：  
boolean数据类型表示一位的信息；  
只有两个取值：true 和 false；  
这种类型只作为一种标志来记录 true/false 情况；  
默认值是 false；  
例子：boolean one = true。  
char：  
char类型是一个单一的 16 位 Unicode 字符；  
最小值是 \u0000（即为0）；  
最大值是 \uffff（即为65,535）；  
char 数据类型可以储存任何字符；  
默认值是 'u0000';  
例子：char letter = 'A';。  
  
引用类型  
在Java中，引用类型的变量非常类似于C/C++的指针。引用类型指向一个对象，指向对象的变量是引用变量。这些变量在声明时被指定为一个特定的类型，比如 Employee、Puppy 等。变量一旦声明后，类型就不能被改变了。  
对象、数组都是引用数据类型。  
所有引用类型的默认值都是null。  
一个引用变量可以用来引用任何与之兼容的类型。  
例子：Site site = new Site("Runoob")。  
  
Java 常量  
常量在程序运行时是不能被修改的。  
在 Java 中使用 final 关键字来修饰常量，声明方式和变量类似：  
final double PI = 3.1415927;  
虽然常量名也可以用小写，但为了便于识别，通常使用大写字母表示常量。  
byte、int、long、和short都可以用十进制、16进制以及8进制的方式来表示。  
当使用常量的时候，前缀 0 表示 8 进制，而前缀 0x 代表 16 进制, 例如：  
int decimal = 100;  
int octal = 0144;  
int hexa =  0x64;  
Java的字符串常量是包含在两个引号之间的字符序列。  
"Hello World"  
"two\nlines"  
"\"This is in quotes\""  
字符串常量和字符常量都可以包含任何Unicode字符。例如：  
char a = '\u0001';  
String a = "\u0001";  
Java语言支持一些特殊的转义字符序列。  
\n	换行 (0x0a)  
\r	回车 (0x0d)  
\f	换页符(0x0c)  
\b	退格 (0x08)  
\0	空字符 (0x20)  
\s	字符串  
\t	制表符  
\"	双引号  
\'	单引号  
\\	反斜杠  
\ddd	八进制字符 (ddd)  
\uxxxx	16进制Unicode字符 (xxxx)  
  
自动类型转换  
整型、实型（常量）、字符型数据可以混合运算。运算中，不同类型的数据先转化为同一类型，然后进行运算。  
转换从低级到高级。  
byte,short,char—> int —> long—> float —> double  
1. 不能对boolean类型进行类型转换。  
2. 不能把对象类型转换成不相关类的对象。  
3. 在把容量大的类型转换为容量小的类型时必须使用强制类型转换。  
4. 转换过程中可能导致溢出或损失精度，例如：  
int i =128;  
byte b = (byte)i;  
因为 byte 类型是 8 位，最大值为127，所以当 int 强制转换为 byte 类型时，值 128 时候就会导致溢出。  
5. 浮点数到整数的转换是通过舍弃小数得到，而不是四舍五入，例如：  
(int)23.7 == 23;  
(int)-45.89f == -45  
必须满足转换前的数据类型的位数要低于转换后的数据类型，例如: short数据类型的位数为16位，就可以自动转换位数为32的int类型，同样float数据类型的位数为32，可以自动转换为64位的double类型。  
  
强制类型转换  
1. 条件是转换的数据类型必须是兼容的。  
2. 格式：(type)value type是要强制类型转换后的数据类型 实例：  
```  
public class TypeConversion{  
    public static void main(String[] args){  
        int i1 = 123;  
        byte b = (byte)i1;//强制类型转换为byte  
        System.out.println("int强制类型转换为byte后的值等于"+b);  
    }  
}  
```  
  
Java 变量类型  
在Java语言中，所有的变量在使用前必须声明。声明变量的基本格式如下：  
type identifier [ = value][, identifier [= value] ...] ;  
格式说明：type为Java数据类型。identifier是变量名。可以使用逗号隔开来声明多个同类型变量。  
以下列出了一些变量的声明实例。注意有些包含了初始化过程。  
int a, b, c;         // 声明三个int型整数：a、 b、c  
int d = 3, e = 4, f = 5; // 声明三个整数并赋予初值  
byte z = 22;         // 声明并初始化 z  
String s = "runoob";  // 声明并初始化字符串 s  
double pi = 3.14159; // 声明了双精度浮点型变量 pi  
char x = 'x';        // 声明变量 x 的值是字符 'x'。  
  
Java语言支持的变量类型有：  
类变量：独立于方法之外的变量，用 static 修饰。  
实例变量：独立于方法之外的变量，不过没有 static 修饰。  
局部变量：类的方法中的变量。  
```  
public class Variable{  
    static int allClicks=0;    // 类变量  
    String str="hello world";  // 实例变量  
    public void method(){  
        int i =0;  // 局部变量  
    }  
}  
```  
  
Java 局部变量  
局部变量声明在方法、构造方法或者语句块中；  
局部变量在方法、构造方法、或者语句块被执行的时候创建，当它们执行完成后，变量将会被销毁；  
访问修饰符不能用于局部变量；  
局部变量只在声明它的方法、构造方法或者语句块中可见；  
局部变量是在栈上分配的。  
局部变量没有默认值，所以局部变量被声明后，必须经过初始化，才可以使用。  
  
实例变量  
实例变量声明在一个类中，但在方法、构造方法和语句块之外；  
当一个对象被实例化之后，每个实例变量的值就跟着确定；  
实例变量在对象创建的时候创建，在对象被销毁的时候销毁；  
实例变量的值应该至少被一个方法、构造方法或者语句块引用，使得外部能够通过这些方式获取实例变量信息；  
实例变量可以声明在使用前或者使用后；  
访问修饰符可以修饰实例变量；  
实例变量对于类中的方法、构造方法或者语句块是可见的。一般情况下应该把实例变量设为私有。通过使用访问修饰符可以使实例变量对子类可见；  
实例变量具有默认值。数值型变量的默认值是0，布尔型变量的默认值是false，引用类型变量的默认值是null。变量的值可以在声明时指定，也可以在构造方法中指定；  
实例变量可以直接通过变量名访问。但在静态方法以及其他类中，就应该使用完全限定名：ObejectReference.VariableName。  
  
类变量（静态变量）  
类变量也称为静态变量，在类中以 static 关键字声明，但必须在方法之外。  
无论一个类创建了多少个对象，类只拥有类变量的一份拷贝。  
静态变量除了被声明为常量外很少使用。常量是指声明为public/private，final和static类型的变量。常量初始化后不可改变。  
静态变量储存在静态存储区。经常被声明为常量，很少单独使用static声明变量。  
静态变量在第一次被访问时创建，在程序结束时销毁。  
与实例变量具有相似的可见性。但为了对类的使用者可见，大多数静态变量声明为public类型。  
默认值和实例变量相似。数值型变量默认值是0，布尔型默认值是false，引用类型默认值是null。变量的值可以在声明的时候指定，也可以在构造方法中指定。此外，静态变量还可以在静态语句块中初始化。  
静态变量可以通过：ClassName.VariableName的方式访问。  
类变量被声明为public static final类型时，类变量名称一般建议使用大写字母。如果静态变量不是public和final类型，其命名方式与实例变量以及局部变量的命名方式一致。  
  
```  
import java.io.*;  
public class Employee {  
    //salary是静态的私有变量  
    private static double salary;  
    // DEPARTMENT是一个常量  
    public static final String DEPARTMENT = "开发人员";  
    public static void main(String[] args){  
    salary = 10000;  
        System.out.println(DEPARTMENT+"平均工资:"+salary);  
    }  
}  
```  
  
Java 修饰符  
访问控制修饰符  
Java中，可以使用访问控制符来保护对类、变量、方法和构造方法的访问。Java 支持 4 种不同的访问权限。  
default (即默认，什么也不写）: 在同一包内可见，不使用任何修饰符。使用对象：类、接口、变量、方法。  
private : 在同一类内可见。使用对象：变量、方法。 注意：不能修饰类（外部类）  
public : 对所有类可见。使用对象：类、接口、变量、方法  
protected : 对同一包内的类和所有子类可见。使用对象：变量、方法。 注意：不能修饰类（外部类）。  
修饰符	当前类	同一包内	子孙类(同一包)	子孙类(不同包)	其他包  
public	Y	Y	Y	Y	Y  
protected	Y	Y	Y	Y/N（说明）	N  
default	Y	Y	Y	N	N  
private	Y	N	N	N	N  
  
默认访问修饰符-不使用任何关键字  
使用默认访问修饰符声明的变量和方法，对同一个包内的类是可见的。接口里的变量都隐式声明为 public static final,而接口里的方法默认情况下访问权限为 public。  
  
私有访问修饰符-private  
私有访问修饰符是最严格的访问级别，所以被声明为 private 的方法、变量和构造方法只能被所属类访问，并且类和接口不能声明为 private。  
声明为私有访问类型的变量只能通过类中公共的 getter 方法被外部类访问。  
Private 访问修饰符的使用主要用来隐藏类的实现细节和保护类的数据。  
  
公有访问修饰符-public  
被声明为 public 的类、方法、构造方法和接口能够被任何其他类访问。  
如果几个相互访问的 public 类分布在不同的包中，则需要导入相应 public 类所在的包。由于类的继承性，类所有的公有方法和变量都能被其子类继承。  
  
受保护的访问修饰符-protected  
protected 需要从以下两个点来分析说明：  
子类与基类在同一包中：被声明为 protected 的变量、方法和构造器能被同一个包中的任何其他类访问；  
子类与基类不在同一包中：那么在子类中，子类实例可以访问其从基类继承而来的 protected 方法，而不能访问基类实例的protected方法。  
  
访问控制和继承  
请注意以下方法继承的规则：  
父类中声明为 public 的方法在子类中也必须为 public。  
父类中声明为 protected 的方法在子类中要么声明为 protected，要么声明为 public，不能声明为 private。  
父类中声明为 private 的方法，不能够被继承。  
  
非访问修饰符  
为了实现一些其他的功能，Java 也提供了许多非访问修饰符。  
static 修饰符，用来修饰类方法和类变量。  
final 修饰符，用来修饰类、方法和变量，final 修饰的类不能够被继承，修饰的方法不能被继承类重新定义，修饰的变量为常量，是不可修改的。  
abstract 修饰符，用来创建抽象类和抽象方法。  
synchronized 和 volatile 修饰符，主要用于线程的编程。  
  
static 修饰符  
静态变量：static 关键字用来声明独立于对象的静态变量，无论一个类实例化多少对象，它的静态变量只有一份拷贝。 静态变量也被称为类变量。局部变量不能被声明为 static 变量。  
静态方法：static 关键字用来声明独立于对象的静态方法。静态方法不能使用类的非静态变量。静态方法从参数列表得到数据，然后计算这些数据。  
对类变量和方法的访问可以直接使用 classname.variablename 和 classname.methodname 的方式访问。  
```  
public class InstanceCounter {  
   private static int numInstances = 0;  
   protected static int getCount() {  
      return numInstances;  
   }  
   private static void addInstance() {  
      numInstances++;  
   }  
   InstanceCounter() {  
      InstanceCounter.addInstance();  
   }  
   public static void main(String[] arguments) {  
      System.out.println("Starting with " +  
      InstanceCounter.getCount() + " instances");  
      for (int i = 0; i < 500; ++i){  
         new InstanceCounter();  
          }  
      System.out.println("Created " +  
      InstanceCounter.getCount() + " instances");  
   }  
}  
```  
  
final 修饰符  
final 变量：  
final 表示"最后的、最终的"含义，变量一旦赋值后，不能被重新赋值。被 final 修饰的实例变量必须显式指定初始值。  
final 修饰符通常和 static 修饰符一起使用来创建类常量。  
final 方法：  
父类中的 final 方法可以被子类继承，但是不能被子类重写。声明 final 方法的主要目的是防止该方法的内容被修改。  
final 类：  
final 类不能被继承，没有类能够继承 final 类的任何特性。  
  
abstract 修饰符  
抽象类：  
抽象类不能用来实例化对象，声明抽象类的唯一目的是为了将来对该类进行扩充。  
一个类不能同时被 abstract 和 final 修饰。如果一个类包含抽象方法，那么该类一定要声明为抽象类，否则将出现编译错误。  
抽象类可以包含抽象方法和非抽象方法。  
抽象方法  
抽象方法是一种没有任何实现的方法，该方法的的具体实现由子类提供。  
抽象方法不能被声明成 final 和 static。  
任何继承抽象类的子类必须实现父类的所有抽象方法，除非该子类也是抽象类。  
如果一个类包含若干个抽象方法，那么该类必须声明为抽象类。抽象类可以不包含抽象方法。  
抽象方法的声明以分号结尾，例如：public abstract sample();。  
  
synchronized 修饰符  
synchronized 关键字声明的方法同一时间只能被一个线程访问。synchronized 修饰符可以应用于四个访问修饰符。  
  
transient 修饰符  
序列化的对象包含被 transient 修饰的实例变量时，java 虚拟机(JVM)跳过该特定的变量。  
该修饰符包含在定义变量的语句中，用来预处理类和变量的数据类型。  
public transient int limit = 55;   // 不会持久化  
public int b; // 持久化  
  
volatile 修饰符  
volatile 修饰的成员变量在每次被线程访问时，都强制从共享内存中重新读取该成员变量的值。而且，当成员变量发生变化时，会强制线程将变化值回写到共享内存。这样在任何时刻，两个不同的线程总是看到某个成员变量的同一个值。  
一个 volatile 对象引用可能是 null。  
  
Java 运算符  
算术运算符  
关系运算符  
位运算符  
逻辑运算符  
赋值运算符  
其他运算符  
  
算术运算符  
假设整数变量A的值为10，变量B的值为20  
+	加法 - 相加运算符两侧的值	A + B 等于 30  
-	减法 - 左操作数减去右操作数	A – B 等于 -10  
*	乘法 - 相乘操作符两侧的值	A * B等于200  
/	除法 - 左操作数除以右操作数	B / A等于2  
％	取余 - 左操作数除以右操作数的余数		B%A等于0  
++	自增: 操作数的值增加1	B++ 或 ++B 等于 21（区别详见下文）  
--	自减: 操作数的值减少1	B-- 或 --B 等于 19（区别详见下文）  
自增自减运算符  
1、自增（++）自减（--）运算符是一种特殊的算术运算符，在算术运算符中需要两个操作数来进行运算，而自增自减运算符是一个操作数。  
2、前缀自增自减法(++a,--a): 先进行自增或者自减运算，再进行表达式运算。  
3、后缀自增自减法(a++,a--): 先进行表达式运算，再进行自增或者自减运算。  
  
关系运算符  
假设整数变量A的值为10，变量B的值为20  
==	检查如果两个操作数的值是否相等，如果相等则条件为真。	（A == B）为假。  
!=	检查如果两个操作数的值是否相等，如果值不相等则条件为真。	(A != B) 为真。  
> 	检查左操作数的值是否大于右操作数的值，如果是那么条件为真。	（A> B）为假。  
< 	检查左操作数的值是否小于右操作数的值，如果是那么条件为真。	（A <B）为真。  
>=	检查左操作数的值是否大于或等于右操作数的值，如果是那么条件为真。	（A> = B）为假。  
<=	检查左操作数的值是否小于或等于右操作数的值，如果是那么条件为真。	（A <= B）为真。  
  
位运算符  
Java定义了位运算符，应用于整数类型(int)，长整型(long)，短整型(short)，字符型(char)，和字节型(byte)等类型。  
位运算符作用在所有的位上，并且按位运算。假设a = 60，b = 13;它们的二进制格式表示将如下：  
A = 0011 1100  
B = 0000 1101  
A&B = 0000 1100  
A | B = 0011 1101  
A ^ B = 0011 0001  
~A= 1100 0011  
假设整数变量 A 的值为 60 和变量 B 的值为 13  
＆	如果相对应位都是1，则结果为1，否则为0	（A＆B），得到12，即0000 1100  
|	如果相对应位都是 0，则结果为 0，否则为 1	（A | B）得到61，即 0011 1101  
^	如果相对应位值相同，则结果为0，否则为1	（A ^ B）得到49，即 0011 0001  
〜	按位取反运算符翻转操作数的每一位，即0变成1，1变成0。	（〜A）得到-61，即1100 0011  
<< 	按位左移运算符。左操作数按位左移右操作数指定的位数。	A << 2得到240，即 1111 0000  
>> 	按位右移运算符。左操作数按位右移右操作数指定的位数。	A >> 2得到15即 1111  
>>> 	按位右移补零操作符。左操作数的值按右操作数指定的位数右移，移动得到的空位以零填充。	A>>>2得到15即0000 1111  
  
逻辑运算符  
假设布尔变量A为真，变量B为假  
&&	称为逻辑与运算符。当且仅当两个操作数都为真，条件才为真。	（A && B）为假。  
| |	称为逻辑或操作符。如果任何两个操作数任何一个为真，条件为真。	（A | | B）为真。  
！	称为逻辑非运算符。用来反转操作数的逻辑状态。如果条件为true，则逻辑非运算符将得到false。	！（A && B）为真。  
  
短路逻辑运算符  
当使用与逻辑运算符时，在两个操作数都为true时，结果才为true，但是当得到第一个操作为false时，其结果就必定是false，这时候就不会再判断第二个操作了。  
```
public class LuoJi{  
    public static void main(String[] args){  
        int a = 5;//定义一个变量；  
        boolean b = (a<4)&&(a++<10);  
        System.out.println("使用短路逻辑运算符的结果为"+b);  
        System.out.println("a的结果为"+a);  
    }  
}  
```
  
赋值运算符  
=	简单的赋值运算符，将右操作数的值赋给左侧操作数	C = A + B将把A + B得到的值赋给C  
+=	加和赋值操作符，它把左操作数和右操作数相加赋值给左操作数	C + = A等价于C = C + A  
-=	减和赋值操作符，它把左操作数和右操作数相减赋值给左操作数	C - = A等价于C = C - A  
*=	乘和赋值操作符，它把左操作数和右操作数相乘赋值给左操作数	C * = A等价于C = C * A  
/=	除和赋值操作符，它把左操作数和右操作数相除赋值给左操作数	C / = A，C 与 A 同类型时等价于 C = C / A  
％=	取模和赋值操作符，它把左操作数和右操作数取模后赋值给左操作数	C％= A等价于C = C％A  
<<=	左移位赋值运算符	C << = 2等价于C = C << 2  
>>=	右移位赋值运算符	C >> = 2等价于C = C >> 2  
＆=	按位与赋值运算符	C＆= 2等价于C = C＆2  
^=	按位异或赋值操作符	C ^ = 2等价于C = C ^ 2  
|=	按位或赋值操作符	C | = 2等价于C = C | 2  
  
条件运算符（?:）  
条件运算符也被称为三元运算符。该运算符有3个操作数，并且需要判断布尔表达式的值。该运算符的主要是决定哪个值应该赋值给变量。  
        variable x = (expression) ? value if true : value if false  
  
instanceof运算符  
该运算符用于操作对象实例，检查该对象是否是一个特定类型（类类型或接口类型）。  
instanceof运算符使用格式如下：  
        ( Object reference variable ) instanceof  (class/interface type)  
如果运算符左侧变量所指的对象，是操作符右侧类或接口(class/interface)的一个对象，那么结果为真。  
String name = "James";  
boolean result = name instanceof String; // 由于 name 是 String 类型，所以返回真  
如果被比较的对象兼容于右侧类型,该运算符仍然返回true。  
```
class Vehicle {}  
public class Car extends Vehicle {  
   public static void main(String[] args){  
      Vehicle a = new Car();  
      boolean result =  a instanceof Car;  
      System.out.println( result);  
   }  
}  
```
  
Java运算符优先级  
下表中具有最高优先级的运算符在的表的最上面，最低优先级的在表的底部。  
类别	操作符	关联性  
后缀	() [] . (点操作符)	左到右  
一元	+ + - ！〜	从右到左  
乘性 	* /％	左到右  
加性 	+ -	左到右  
移位 	>> >>>  << 	左到右  
关系 	>> = << = 	左到右  
相等 	==  !=	左到右  
按位与	＆	左到右  
按位异或	^	左到右  
按位或	|	左到右  
逻辑与	&&	左到右  
逻辑或	| |	左到右  
条件	？：	从右到左  
赋值	= + = - = * = / =％= >> = << =＆= ^ = | =	从右到左  
逗号	，	左到右  
  
Java 循环结构 - for, while 及 do...while  
Java中有三种主要的循环结构：  
while 循环  
do…while 循环  
for 循环  
  
while 循环  
while是最基本的循环，它的结构为：  
while( 布尔表达式 ) {  
  //循环内容  
}  
只要布尔表达式为 true，循环就会一直执行下去。  
  
do…while 循环  
对于 while 语句而言，如果不满足条件，则不能进入循环。但有时候我们需要即使不满足条件，也至少执行一次。  
do…while 循环和 while 循环相似，不同的是，do…while 循环至少会执行一次。  
do {  
       //代码语句  
}while(布尔表达式);  
  
for循环  
虽然所有循环结构都可以用 while 或者 do...while表示，但 Java 提供了另一种语句 —— for 循环，使一些循环结构变得更加简单。  
for循环执行的次数是在执行前就确定的。语法格式如下：  
for(初始化; 布尔表达式; 更新) {  
    //代码语句  
}  
最先执行初始化步骤。可以声明一种类型，但可初始化一个或多个循环控制变量，也可以是空语句。  
然后，检测布尔表达式的值。如果为 true，循环体被执行。如果为false，循环终止，开始执行循环体后面的语句。  
执行一次循环后，更新循环控制变量。  
再次检测布尔表达式。循环执行上面的过程。  
  
Java 增强 for 循环  
Java5 引入了一种主要用于数组的增强型 for 循环。  
Java 增强 for 循环语法格式如下:  
for(声明语句 : 表达式)  
{  
   //代码句子  
}  
声明语句：声明新的局部变量，该变量的类型必须和数组元素的类型匹配。其作用域限定在循环语句块，其值与此时数组元素的值相等。  
表达式：表达式是要访问的数组名，或者是返回值为数组的方法。  
```  
public class Test {  
   public static void main(String args[]){  
      int [] numbers = {10, 20, 30, 40, 50};  
  
      for(int x : numbers ){  
         System.out.print( x );  
         System.out.print(",");  
      }  
      System.out.print("\n");  
      String [] names ={"James", "Larry", "Tom", "Lacy"};  
      for( String name : names ) {  
         System.out.print( name );  
         System.out.print(",");  
      }  
   }  
}  
```  
  
break 关键字  
break 主要用在循环语句或者 switch 语句中，用来跳出整个语句块。  
break 跳出最里层的循环，并且继续执行该循环下面的语句。  
  
continue 关键字  
continue 适用于任何循环控制结构中。作用是让程序立刻跳转到下一次循环的迭代。  
在 for 循环中，continue 语句使程序立即跳转到更新语句。  
在 while 或者 do…while 循环中，程序立即跳转到布尔表达式的判断语句。  
  
Java 条件语句 - if...else  
一个 if 语句包含一个布尔表达式和一条或多条语句。  
语法  
if 语句的语法如下：  
```  
if(布尔表达式)  
{  
   //如果布尔表达式为true将执行的语句  
}  
```  
如果布尔表达式的值为 true，则执行 if 语句中的代码块，否则执行 if 语句块后面的代码。  
  
if...else语句  
if 语句后面可以跟 else 语句，当 if 语句的布尔表达式值为 false 时，else 语句块会被执行。  
语法  
if…else 的用法如下：  
```  
if(布尔表达式){  
   //如果布尔表达式的值为true  
}else{  
   //如果布尔表达式的值为false  
}  
```  
  
if...else if...else 语句  
if 语句后面可以跟 else if…else 语句，这种语句可以检测到多种可能的情况。  
使用 if，else if，else 语句的时候，需要注意下面几点：  
if 语句至多有 1 个 else 语句，else 语句在所有的 else if 语句之后。  
if 语句可以有若干个 else if 语句，它们必须在 else 语句之前。  
一旦其中一个 else if 语句检测为 true，其他的 else if 以及 else 语句都将跳过执行。  
语法  
if...else 语法格式如下:  
```  
if(布尔表达式 1){  
   //如果布尔表达式 1的值为true执行代码  
}else if(布尔表达式 2){  
   //如果布尔表达式 2的值为true执行代码  
}else if(布尔表达式 3){  
   //如果布尔表达式 3的值为true执行代码  
}else {  
   //如果以上布尔表达式都不为true执行代码  
}  
```  
  
嵌套的 if…else 语句  
使用嵌套的 if…else 语句是合法的。也就是说你可以在另一个 if 或者 else if 语句中使用 if 或者 else if 语句。  
语法  
嵌套的 if…else 语法格式如下：  
```  
if(布尔表达式 1){  
   ////如果布尔表达式 1的值为true执行代码  
   if(布尔表达式 2){  
      ////如果布尔表达式 2的值为true执行代码  
   }  
}  
```  
  
Java switch case 语句  
switch case 语句判断一个变量与一系列值中某个值是否相等，每个值称为一个分支。  
语法  
switch case 语句语法格式如下：  
```  
switch(expression){  
    case value :  
       //语句  
       break; //可选  
    case value :  
       //语句  
       break; //可选  
    //你可以有任意数量的case语句  
    default : //可选  
       //语句  
}  
```  
switch case 语句有如下规则：  
switch 语句中的变量类型可以是： byte、short、int 或者 char。从 Java SE 7 开始，switch 支持字符串 String 类型了，同时 case 标签必须为字符串常量或字面量。  
switch 语句可以拥有多个 case 语句。每个 case 后面跟一个要比较的值和冒号。  
case 语句中的值的数据类型必须与变量的数据类型相同，而且只能是常量或者字面常量。  
当变量的值与 case 语句的值相等时，那么 case 语句之后的语句开始执行，直到 break 语句出现才会跳出 switch 语句。  
当遇到 break 语句时，switch 语句终止。程序跳转到 switch 语句后面的语句执行。case 语句不必须要包含 break 语句。如果没有 break 语句出现，程序会继续执行下一条 case 语句，直到出现 break 语句。  
switch 语句可以包含一个 default 分支，该分支一般是 switch 语句的最后一个分支（可以在任何位置，但建议在最后一个）。default 在没有 case 语句的值和变量值相等的时候执行。default 分支不需要 break 语句。  
switch case 执行时，一定会先进行匹配，匹配成功返回当前 case 的值，再根据是否有 break，判断是否继续输出，或是跳出判断。  
如果 case 语句块中没有 break 语句时，JVM 并不会顺序输出每一个 case 对应的返回值，而是继续匹配，匹配不成功则返回默认 case。  
如果当前匹配成功的 case 语句块没有 break 语句，则从当前 case 开始，后续所有 case 的值都会输出，如果后续的 case 语句块有 break 语句则会跳出判断。  
  
Java Number & Math 类  
Java 语言为每一个内置数据类型提供了对应的包装类。  
所有的包装类（Integer、Long、Byte、Double、Float、Short）都是抽象类 Number 的子类。  
基本类型	包装类  
double	Double  
float	Float  
long	Long  
int		Integer  
short	Short  
byte	Byte  
char	Character  
boolean	Boolean  
  
Java Math 类  
Java 的 Math 包含了用于执行基本数学运算的属性和方法，如初等指数、对数、平方根和三角函数。  
Math 的方法都被定义为 static 形式，通过 Math 类可以在主函数中直接调用。  
```  
public class Test {  
    public static void main (String []args)  
    {  
        System.out.println("90 度的正弦值：" + Math.sin(Math.PI/2));  
        System.out.println("0度的余弦值：" + Math.cos(0));  
        System.out.println("60度的正切值：" + Math.tan(Math.PI/3));  
        System.out.println("1的反正切值： " + Math.atan(1));  
        System.out.println("π/2的角度值：" + Math.toDegrees(Math.PI/2));  
        System.out.println(Math.PI);  
    }  
}  
```  
  
Number & Math 类方法  
1. xxxValue()  将 Number 对象转换为xxx数据类型的值并返回。  
2. compareTo()  将number对象与参数比较。  
3. equals()  判断number对象是否与参数相等。  
4. valueOf()  返回一个 Number 对象指定的内置数据类型  
5. toString()  以字符串形式返回值。  
6. parseInt()  将字符串解析为int类型。  
7. abs()  返回参数的绝对值。  
8. ceil()  返回大于等于( >= )给定参数的的最小整数，类型为双精度浮点型。  
9. floor()  返回小于等于（<=）给定参数的最大整数 。  
10. rint()  返回与参数最接近的整数。返回类型为double。  
11. round()  它表示四舍五入，算法为 Math.floor(x+0.5)，即将原来的数字加上 0.5 后再向下取整，所以，Math.round(11.5) 的结果为12，Math.round(-11.5) 的结果为-11。  
12. min()  返回两个参数中的最小值。  
13. max()  返回两个参数中的最大值。  
14. exp()  返回自然数底数e的参数次方。  
15. log()  返回参数的自然数底数的对数值。  
16. pow()  返回第一个参数的第二个参数次方。  
17. sqrt()  求参数的算术平方根。  
18. sin()  求指定double类型参数的正弦值。  
19. cos()  求指定double类型参数的余弦值。  
20. tan()  求指定double类型参数的正切值。  
21. asin()  求指定double类型参数的反正弦值。  
22. acos()  求指定double类型参数的反余弦值。  
23. atan()  求指定double类型参数的反正切值。  
24. atan2()  将笛卡尔坐标转换为极坐标，并返回极坐标的角度值。  
25. toDegrees()  将参数转化为角度。  
26. toRadians()  将角度转换为弧度。  
27. random()  返回一个随机数。  

Java Character 类  
Java语言为内置数据类型char提供了包装类Character类。  
Character ch = new Character('a');  
下面是Character类的方法：  
1. isLetter()是否是一个字母  
2. isDigit()是否是一个数字字符  
3. isWhitespace()是否是一个空白字符  
4. isUpperCase()是否是大写字母  
5. isLowerCase()是否是小写字母  
6. toUpperCase()指定字母的大写形式  
7. toLowerCase()指定字母的小写形式  
8. toString()返回字符的字符串形式，字符串的长度仅为1  
  
Java String 类  
Java 提供了 String 类来创建和操作字符串。  
String greeting = "菜鸟教程";  
String 类有 11 种构造方法，这些方法提供不同的参数来初始化字符串，比如提供一个字符数组参数:  
```  
public class StringDemo{  
   public static void main(String args[]){  
      char[] helloArray = { 'r', 'u', 'n', 'o', 'o', 'b'};  
      String helloString = new String(helloArray);  
      System.out.println( helloString );  
   }  
}  
```  
  
字符串长度  
String 类的一个访问器方法是 length() 方法，它返回字符串对象包含的字符数。  
```  
public class StringDemo {  
    public static void main(String args[]) {  
        String site = "www.runoob.com";  
        int len = site.length();  
        System.out.println( "菜鸟教程网址长度 : " + len );  
   }  
}  
```  
  
连接字符串  
String 类提供了连接两个字符串的方法：  
string1.concat(string2);  
返回 string2 连接 string1 的新字符串。也可以对字符串常量使用 concat() 方法，如  
```  
public class StringDemo {  
    public static void main(String args[]) {  
        String string1 = "菜鸟教程网址：";  
        System.out.println("1、" + string1 + "www.runoob.com");  
    }  
}  
```  
  
创建格式化字符串  
我们知道输出格式化数字可以使用 printf() 和 format() 方法。  
String 类使用静态方法 format() 返回一个String 对象而不是 PrintStream 对象。  
String 类的静态方法 format() 能用来创建可复用的格式化字符串，而不仅仅是用于一次打印输出。  
```  
String fs;  
fs = String.format("浮点型变量的值为 " +  
                   "%f, 整型变量的值为 " +  
                   " %d, 字符串变量的值为 " +  
                   " %s", floatVar, intVar, stringVar);  
```  
  
String 方法  
1. char charAt(int index) 返回指定索引处的 char 值。  
2. int compareTo(Object o) 把这个字符串和另一个对象比较。  
3. int compareTo(String anotherString) 按字典顺序比较两个字符串。  
4. int compareToIgnoreCase(String str) 按字典顺序比较两个字符串，不考虑大小写。  
5. String concat(String str) 将指定字符串连接到此字符串的结尾。  
6. boolean contentEquals(StringBuffer sb) 当且仅当字符串与指定的StringBuffer有相同顺序的字符时候返回真。  
7. static String copyValueOf(char[] data) 返回指定数组中表示该字符序列的 String。  
8. static String copyValueOf(char[] data, int offset, int count) 返回指定数组中表示该字符序列的 String。  
9. boolean endsWith(String suffix) 测试此字符串是否以指定的后缀结束。  
10. boolean equals(Object anObject) 将此字符串与指定的对象比较。  
11. boolean equalsIgnoreCase(String anotherString) 将此 String 与另一个 String 比较，不考虑大小写。  
12. byte[] getBytes() 使用平台的默认字符集将此 String 编码为 byte 序列，并将结果存储到一个新的 byte 数组中。  
13. byte[] getBytes(String charsetName) 使用指定的字符集将此 String 编码为 byte 序列，并将结果存储到一个新的 byte 数组中。  
14. void getChars(int srcBegin, int srcEnd, char[] dst, int dstBegin) 将字符从此字符串复制到目标字符数组。  
15. int hashCode() 返回此字符串的哈希码。  
16. int indexOf(int ch) 返回指定字符在此字符串中第一次出现处的索引。  
17. int indexOf(int ch, int fromIndex) 返回在此字符串中第一次出现指定字符处的索引，从指定的索引开始搜索。  
18. int indexOf(String str) 返回指定子字符串在此字符串中第一次出现处的索引。  
19. int indexOf(String str, int fromIndex) 返回指定子字符串在此字符串中第一次出现处的索引，从指定的索引开始。  
20. String intern() 返回字符串对象的规范化表示形式。  
21. int lastIndexOf(int ch) 返回指定字符在此字符串中最后一次出现处的索引。  
22. int lastIndexOf(int ch, int fromIndex) 返回指定字符在此字符串中最后一次出现处的索引，从指定的索引处开始进行反向搜索。  
23. int lastIndexOf(String str) 返回指定子字符串在此字符串中最右边出现处的索引。  
24. int lastIndexOf(String str, int fromIndex) 返回指定子字符串在此字符串中最后一次出现处的索引，从指定的索引开始反向搜索。  
25. int length() 返回此字符串的长度。  
26. boolean matches(String regex) 告知此字符串是否匹配给定的正则表达式。  
27. boolean regionMatches(boolean ignoreCase, int toffset, String other, int ooffset, int len) 测试两个字符串区域是否相等。  
28. boolean regionMatches(int toffset, String other, int ooffset, int len) 测试两个字符串区域是否相等。  
29. String replace(char oldChar, char newChar) 返回一个新的字符串，它是通过用 newChar 替换此字符串中出现的所有 oldChar 得到的。  
30. String replaceAll(String regex, String replacement) 使用给定的 replacement 替换此字符串所有匹配给定的正则表达式的子字符串。  
31. String replaceFirst(String regex, String replacement) 使用给定的 replacement 替换此字符串匹配给定的正则表达式的第一个子字符串。  
32. String[] split(String regex) 根据给定正则表达式的匹配拆分此字符串。  
33. String[] split(String regex, int limit) 根据匹配给定的正则表达式来拆分此字符串。  
34. boolean startsWith(String prefix) 测试此字符串是否以指定的前缀开始。  
35. boolean startsWith(String prefix, int toffset) 测试此字符串从指定索引开始的子字符串是否以指定前缀开始。  
36. CharSequence subSequence(int beginIndex, int endIndex) 返回一个新的字符序列，它是此序列的一个子序列。  
37. String substring(int beginIndex) 返回一个新的字符串，它是此字符串的一个子字符串。  
38. String substring(int beginIndex, int endIndex) 返回一个新字符串，它是此字符串的一个子字符串。  
39. char[] toCharArray() 将此字符串转换为一个新的字符数组。  
40. String toLowerCase() 使用默认语言环境的规则将此 String 中的所有字符都转换为小写。  
41. String toLowerCase(Locale locale) 使用给定 Locale 的规则将此 String 中的所有字符都转换为小写。  
42. String toString() 返回此对象本身（它已经是一个字符串！）。  
43. String toUpperCase() 使用默认语言环境的规则将此 String 中的所有字符都转换为大写。  
44. String toUpperCase(Locale locale) 使用给定 Locale 的规则将此 String 中的所有字符都转换为大写。  
45. String trim() 返回字符串的副本，忽略前导空白和尾部空白。  
46. static String valueOf(primitive data type x) 返回给定data type类型x参数的字符串表示形式。  
  
Java StringBuffer 和 StringBuilder 类  
当对字符串进行修改的时候，需要使用 StringBuffer 和 StringBuilder 类。  
由于 StringBuilder 相较于 StringBuffer 有速度优势，所以多数情况下建议使用 StringBuilder 类。然而在应用程序要求线程安全的情况下，则必须使用 StringBuffer 类。  
```  
public class Test{  
  public static void main(String args[]){  
    StringBuffer sBuffer = new StringBuffer("菜鸟教程官网：");  
    sBuffer.append("www");  
    sBuffer.append(".runoob");  
    sBuffer.append(".com");  
    System.out.println(sBuffer);  
  }  
}  
```  
  
StringBuffer 方法  
1. public StringBuffer append(String s) 将指定的字符串追加到此字符序列。  
2. public StringBuffer reverse() 将此字符序列用其反转形式取代。  
3. public delete(int start, int end) 移除此序列的子字符串中的字符。  
4. public insert(int offset, int i) 将 int 参数的字符串表示形式插入此序列中。  
5. replace(int start, int end, String str) 使用给定 String 中的字符替换此序列的子字符串中的字符。  
下面的列表里的方法和 String 类的方法类似：  
1. int capacity() 返回当前容量。  
2. char charAt(int index) 返回此序列中指定索引处的 char 值。  
3. void ensureCapacity(int minimumCapacity) 确保容量至少等于指定的最小值。  
4. void getChars(int srcBegin, int srcEnd, char[] dst, int dstBegin) 将字符从此序列复制到目标字符数组 dst。  
5. int indexOf(String str) 返回第一次出现的指定子字符串在该字符串中的索引。  
6. int indexOf(String str, int fromIndex) 从指定的索引处开始，返回第一次出现的指定子字符串在该字符串中的索引。  
7. int lastIndexOf(String str) 返回最右边出现的指定子字符串在此字符串中的索引。  
8. int lastIndexOf(String str, int fromIndex) 返回 String 对象中子字符串最后出现的位置。  
9. int length() 返回长度（字符数）。  
10.  void setCharAt(int index, char ch) 将给定索引处的字符设置为 ch。  
11.  void setLength(int newLength) 设置字符序列的长度。  
12.  CharSequence subSequence(int start, int end) 返回一个新的字符序列，该字符序列是此序列的子序列。  
13.  String substring(int start) 返回一个新的 String，它包含此字符序列当前所包含的字符子序列。  
14.  String substring(int start, int end) 返回一个新的 String，它包含此序列当前所包含的字符子序列。  
15.  String toString() 返回此序列中数据的字符串表示形式。  
  
Java 数组  
Java 语言中提供的数组是用来存储固定大小的同类型元素。  
声明数组变量  
首先必须声明数组变量，才能在程序中使用数组。下面是声明数组变量的语法：  
dataType[] arrayRefVar;   // 首选的方法  
或  
dataType arrayRefVar[];  // 效果相同，但不是首选方法  
  
创建数组  
Java语言使用new操作符来创建数组，语法如下：  
arrayRefVar = new dataType[arraySize];  
上面的语法语句做了两件事：  
一、使用 dataType[arraySize] 创建了一个数组。  
二、把新创建的数组的引用赋值给变量 arrayRefVar。  
数组变量的声明，和创建数组可以用一条语句完成，如下所示：  
dataType[] arrayRefVar = new dataType[arraySize];  
另外，你还可以使用如下的方式创建数组。  
dataType[] arrayRefVar = {value0, value1, ..., valuek};  
数组的元素是通过索引访问的。数组索引从 0 开始，所以索引值从 0 到 arrayRefVar.length-1。  
  
处理数组  
数组的元素类型和数组的大小都是确定的，所以当处理数组元素时候，我们通常使用基本循环或者 For-Each 循环。  
```  
public class TestArray {  
   public static void main(String[] args) {  
      double[] myList = {1.9, 2.9, 3.4, 3.5};  
      // 打印所有数组元素  
      for (int i = 0; i < myList.length; i++) {  
         System.out.println(myList[i] + " ");  
      }  
      // 计算所有元素的总和  
      double total = 0;  
      for (int i = 0; i < myList.length; i++) {  
         total += myList[i];  
      }  
      System.out.println("Total is " + total);  
      // 查找最大元素  
      double max = myList[0];  
      for (int i = 1; i < myList.length; i++) {  
         if (myList[i] > max) max = myList[i];  
      }  
      System.out.println("Max is " + max);  
      // 打印所有数组元素  
      for (double element: myList) {  
         System.out.println(element);  
      }  
   }  
}  
```  
  
数组作为函数的参数  
数组可以作为参数传递给方法。  
```  
public static void printArray(int[] array) {  
  for (int i = 0; i < array.length; i++) {  
    System.out.print(array[i] + " ");  
  }  
}  
printArray(new int[]{3, 1, 2, 6, 4, 2});  
```  
  
数组作为函数的返回值  
```  
public static int[] reverse(int[] list) {  
  int[] result = new int[list.length];  
  for (int i = 0, j = result.length - 1; i < list.length; i++, j--) {  
    result[j] = list[i];  
  }  
  return result;  
}  
```  
  
多维数组  
多维数组可以看成是数组的数组，比如二维数组就是一个特殊的一维数组，其每一个元素都是一个一维数组，例如：  
String str[][] = new String[3][4];  
多维数组的动态初始化（以二维数组为例）  
1. 直接为每一维分配空间，格式如下：  
type[][] typeName = new type[typeLength1][typeLength2];  
type 可以为基本数据类型和复合数据类型，arraylength1 和 arraylength2 必须为正整数，arraylength1 为行数，arraylength2 为列数。例如：  
int a[][] = new int[2][3]; //二维数组 a 可以看成一个两行三列的数组。  
2. 从最高维开始，分别为每一维分配空间，例如：  
```  
String s[][] = new String[2][];  
s[0] = new String[2];  
s[1] = new String[3];  
s[0][0] = new String("Good");  
s[0][1] = new String("Luck");  
s[1][0] = new String("to");  
s[1][1] = new String("you");  
s[1][2] = new String("!");  
```  
解析：  
s[0]=new String[2] 和 s[1]=new String[3] 是为最高维分配引用空间，也就是为最高维限制其能保存数据的最长的长度，然后再为其每个数组元素单独分配空间 s0=new String("Good") 等操作。  
  
Arrays 类  
java.util.Arrays 类能方便地操作数组，它提供的所有方法都是静态的。  
具有以下功能：  
给数组赋值：通过 fill 方法。  
对数组排序：通过 sort 方法,按升序。  
比较数组：通过 equals 方法比较数组中元素值是否相等。  
查找数组元素：通过 binarySearch 方法能对排序好的数组进行二分查找法操作。  
1 public static int binarySearch(Object[] a, Object key)  
用二分查找算法在给定数组中搜索给定值的对象(Byte,Int,double等)。数组在调用前必须排序好的。如果查找值包含在数组中，则返回搜索键的索引；否则返回 (-(插入点) - 1)。  
2 public static boolean equals(long[] a, long[] a2)  
如果两个指定的 long 型数组彼此相等，则返回 true。如果两个数组包含相同数量的元素，并且两个数组中的所有相应元素对都是相等的，则认为这两个数组是相等的。换句话说，如果两个数组以相同顺序包含相同的元素，则两个数组是相等的。同样的方法适用于所有的其他基本数据类型（Byte，short，Int等）。  
3 public static void fill(int[] a, int val)  
将指定的 int 值分配给指定 int 型数组指定范围中的每个元素。同样的方法适用于所有的其他基本数据类型（Byte，short，Int等）。  
4 public static void sort(Object[] a)  
对指定对象数组根据其元素的自然顺序进行升序排列。同样的方法适用于所有的其他基本数据类型（Byte，short，Int等）。  
  
Java 方法  
Java方法是语句的集合，它们在一起执行一个功能。  
方法是解决一类问题的步骤的有序组合  
方法包含于类或对象中  
方法在程序中被创建，在其他地方被引用  
方法的命名规则  
1.方法的名字的第一个单词应以小写字母作为开头，后面的单词则用大写字母开头写，不使用连接符。例如：addPerson。  
2.下划线可能出现在 JUnit 测试方法名称中用以分隔名称的逻辑组件。一个典型的模式是：test<MethodUnderTest>_<state>，例如 testPop_emptyStack。  
  
方法的定义  
一般情况下，定义一个方法包含以下语法：  
```  
修饰符 返回值类型 方法名(参数类型 参数名){  
    ...  
    方法体  
    ...  
    return 返回值;  
}  
```  
方法包含一个方法头和一个方法体。下面是一个方法的所有部分：  
修饰符：修饰符，这是可选的，告诉编译器如何调用该方法。定义了该方法的访问类型。  
返回值类型 ：方法可能会返回值。returnValueType 是方法返回值的数据类型。有些方法执行所需的操作，但没有返回值。在这种情况下，returnValueType 是关键字void。  
方法名：是方法的实际名称。方法名和参数表共同构成方法签名。  
参数类型：参数像是一个占位符。当方法被调用时，传递值给参数。这个值被称为实参或变量。参数列表是指方法的参数类型、顺序和参数的个数。参数是可选的，方法可以不包含任何参数。  
方法体：方法体包含具体的语句，定义该方法的功能。  
```  
public static int max(int num1, int num2) {  
   int result;  
   if (num1 > num2)  result = num1;  
   else  result = num2;  
   return result;  
}  
```  
  
方法调用  
Java 支持两种调用方法的方式，根据方法是否返回值来选择。  
当程序调用一个方法时，程序的控制权交给了被调用的方法。当被调用方法的返回语句执行或者到达方法体闭括号时候交还控制权给程序。  
当方法返回一个值的时候，方法调用通常被当做一个值。例如：  
int larger = max(30, 40);  
如果方法返回值是void，方法调用一定是一条语句。例如，方法println返回void。下面的调用是个语句：  
System.out.println("欢迎访问菜鸟教程！");  
  
通过值传递参数  
调用一个方法时候需要提供参数，你必须按照参数列表指定的顺序提供。  
  
方法的重载  
上面使用的max方法仅仅适用于int型数据。但如果你想得到两个浮点类型数据的最大值呢？  
解决方法是创建另一个有相同名字但参数不同的方法，如下面代码所示：  
```  
public static double max(double num1, double num2) {  
  if (num1 > num2)  
    return num1;  
  else  
    return num2;  
}  
```  
Java编译器根据方法签名判断哪个方法应该被调用。  
方法重载可以让程序更清晰易读。执行密切相关任务的方法应该使用相同的名字。  
重载的方法必须拥有不同的参数列表。你不能仅仅依据修饰符或者返回类型的不同来重载方法。  
  
命令行参数的使用  
有时候你希望运行一个程序时候再传递给它消息。这要靠传递命令行参数给main()函数实现。  
命令行参数是在执行程序时候紧跟在程序名字后面的信息。  
CommandLine.java 文件代码：  
```  
public class CommandLine {  
   public static void main(String args[]){  
      for(int i=0; i<args.length; i++){  
         System.out.println("args[" + i + "]: " + args[i]);  
      }  
   }  
}  
```  
  
可变参数  
Java支持传递同类型的可变参数给一个方法。  
方法的可变参数的声明如下所示：  
typeName... parameterName  
在方法声明中，在指定参数类型后加一个省略号(...) 。  
一个方法中只能指定一个可变参数，它必须是方法的最后一个参数。任何普通的参数必须在它之前声明。  
  
finalize() 方法  
Java 允许定义这样的方法，它在对象被垃圾收集器析构(回收)之前调用，这个方法叫做 finalize( )，它用来清除回收对象。  
例如，你可以使用 finalize() 来确保一个对象打开的文件被关闭了。  
在 finalize() 方法里，你必须指定在对象销毁时候要执行的操作。  
finalize() 一般格式是：  
```
protected void finalize()  
{  
   // 在这里终结代码  
}  
```
关键字 protected 是一个限定符，它确保 finalize() 方法不会被该类以外的代码调用。  
当然，Java 的内存回收可以由 JVM 来自动完成。如果你手动使用，则可以使用上面的方法。  
```  
public class FinalizationDemo {  
  public static void main(String[] args) {  
    Cake c1 = new Cake(1);  
    Cake c2 = new Cake(2);  
    Cake c3 = new Cake(3);  
    c2 = c3 = null;  
    System.gc(); //调用Java垃圾收集器  
  }  
}  
class Cake extends Object {  
  private int id;  
  public Cake(int id) {  
    this.id = id;  
    System.out.println("Cake Object " + id + " is created");  
  }  
  protected void finalize() throws java.lang.Throwable {  
    super.finalize();  
    System.out.println("Cake Object " + id + " is disposed");  
  }  
}  
```  
  
Java 异常处理  
异常是程序中的一些错误，但并不是所有的错误都是异常，并且错误有时候是可以避免的。  
三种类型的异常：  
检查性异常：最具代表的检查性异常是用户错误或问题引起的异常，这是程序员无法预见的。例如要打开一个不存在文件时，一个异常就发生了，这些异常在编译时不能被简单地忽略。  
运行时异常： 运行时异常是可能被程序员避免的异常。与检查性异常相反，运行时异常可以在编译时被忽略。  
错误： 错误不是异常，而是脱离程序员控制的问题。错误在代码中通常被忽略。例如，当栈溢出时，一个错误就发生了，它们在编译也检查不到的。  
  
Exception 类的层次  
所有的异常类是从 java.lang.Exception 类继承的子类。  
Exception 类是 Throwable 类的子类。除了Exception类外，Throwable还有一个子类Error 。  
异常类有两个主要的子类：IOException 类和 RuntimeException 类。  
Java 内置异常类  
Java 语言定义了一些异常类在 java.lang 标准包中。  
标准运行时异常类的子类是最常见的异常类。由于 java.lang 包是默认加载到所有的 Java 程序的，所以大部分从运行时异常类继承而来的异常都可以直接使用。  
Java 根据各个类库也定义了一些其他的异常，下面的表中列出了 Java 的非检查性异常。  
ArithmeticException 当出现异常的运算条件时，抛出此异常。例如，一个整数"除以零"时，抛出此类的一个实例。  
ArrayIndexOutOfBoundsException  用非法索引访问数组时抛出的异常。如果索引为负或大于等于数组大小，则该索引为非法索引。  
ArrayStoreException 试图将错误类型的对象存储到一个对象数组时抛出的异常。  
ClassCastException  当试图将对象强制转换为不是实例的子类时，抛出该异常。  
IllegalArgumentException  抛出的异常表明向方法传递了一个不合法或不正确的参数。  
IllegalMonitorStateException  抛出的异常表明某一线程已经试图等待对象的监视器，或者试图通知其他正在等待对象的监视器而本身没有指定监视器的线程。  
IllegalStateException 在非法或不适当的时间调用方法时产生的信号。换句话说，即 Java 环境或 Java 应用程序没有处于请求操作所要求的适当状态下。  
IllegalThreadStateException 线程没有处于请求操作所要求的适当状态时抛出的异常。  
IndexOutOfBoundsException 指示某排序索引（例如对数组、字符串或向量的排序）超出范围时抛出。  
NegativeArraySizeException  如果应用程序试图创建大小为负的数组，则抛出该异常。  
NullPointerException  当应用程序试图在需要对象的地方使用 null 时，抛出该异常  
NumberFormatException 当应用程序试图将字符串转换成一种数值类型，但该字符串不能转换为适当格式时，抛出该异常。  
SecurityException 由安全管理器抛出的异常，指示存在安全侵犯。  
StringIndexOutOfBoundsException 此异常由 String 方法抛出，指示索引或者为负，或者超出字符串的大小。  
UnsupportedOperationException 当不支持请求的操作时，抛出该异常。  
下面的表中列出了 Java 定义在 java.lang 包中的检查性异常类。  
ClassNotFoundException  应用程序试图加载类时，找不到相应的类，抛出该异常。  
CloneNotSupportedException  当调用 Object 类中的 clone 方法克隆对象，但该对象的类无法实现 Cloneable 接口时，抛出该异常。  
IllegalAccessException  拒绝访问一个类的时候，抛出该异常。  
InstantiationException  当试图使用 Class 类中的 newInstance 方法创建一个类的实例，而指定的类对象因为是一个接口或是一个抽象类而无法实例化时，抛出该异常。  
InterruptedException  一个线程被另一个线程中断，抛出该异常。  
NoSuchFieldException  请求的变量不存在  
NoSuchMethodException 请求的方法不存在  
  
异常方法  
下面的列表是 Throwable 类的主要方法:  
1. public String getMessage()  返回关于发生的异常的详细信息。这个消息在Throwable 类的构造函数中初始化了。  
2. public Throwable getCause()  返回一个Throwable 对象代表异常原因。  
3. public String toString()  使用getMessage()的结果返回类的串级名字。  
4. public void printStackTrace()  打印toString()结果和栈层次到System.err，即错误输出流。  
5. public StackTraceElement [] getStackTrace()  返回一个包含堆栈层次的数组。下标为0的元素代表栈顶，最后一个元素代表方法调用堆栈的栈底。  
6. public Throwable fillInStackTrace()  用当前的调用栈层次填充Throwable 对象栈层次，添加到栈层次任何先前信息中。  
  
捕获异常  
使用 try 和 catch 关键字可以捕获异常。try/catch 代码块放在异常可能发生的地方。  
try/catch代码块中的代码称为保护代码，使用 try/catch 的语法如下：  
```
try  
{  
   // 程序代码  
}catch(ExceptionName e1)  
{  
   //Catch 块  
}  
```
Catch 语句包含要捕获异常类型的声明。当保护代码块中发生一个异常时，try 后面的 catch 块就会被检查。  
如果发生的异常包含在 catch 块中，异常会被传递到该 catch 块，这和传递一个参数到方法是一样。  
  
多重捕获块  
一个 try 代码块后面跟随多个 catch 代码块的情况就叫多重捕获。  
多重捕获块的语法如下所示：  
```
try{  
   // 程序代码  
}catch(异常类型1 异常的变量名1){  
  // 程序代码  
}catch(异常类型2 异常的变量名2){  
  // 程序代码  
}catch(异常类型2 异常的变量名2){  
  // 程序代码  
}  
```
可以在 try 语句后面添加任意数量的 catch 块。  
如果保护代码中发生异常，异常被抛给第一个 catch 块。  
如果抛出异常的数据类型与 ExceptionType1 匹配，它在这里就会被捕获。  
如果不匹配，它会被传递给第二个 catch 块。  
如此，直到异常被捕获或者通过所有的 catch 块。  
  
throws/throw 关键字：  
如果一个方法没有捕获到一个检查性异常，那么该方法必须使用 throws 关键字来声明。throws 关键字放在方法签名的尾部。  
也可以使用 throw 关键字抛出一个异常，无论它是新实例化的还是刚捕获到的。  
下面方法的声明抛出一个 RemoteException 异常：  
```  
import java.io.\*;  
public class className  
{  
  public void deposit(double amount) throws RemoteException  
  {  
    // Method implementation  
    throw new RemoteException();  
  }  
  //Remainder of class definition  
}  
```  
一个方法可以声明抛出多个异常，多个异常之间用逗号隔开。  
  
finally关键字  
finally 关键字用来创建在 try 代码块后面执行的代码块。  
无论是否发生异常，finally 代码块中的代码总会被执行。  
在 finally 代码块中，可以运行清理类型等收尾善后性质的语句。  
finally 代码块出现在 catch 代码块最后，语法如下：  
```  
try{  
  // 程序代码  
}catch(异常类型1 异常的变量名1){  
  // 程序代码  
}catch(异常类型2 异常的变量名2){  
  // 程序代码  
}finally{  
  // 程序代码  
}  
```  
```  
public class ExcepTest{  
  public static void main(String args[]){  
    int a[] = new int[2];  
    try{  
       System.out.println("Access element three :" + a[3]);  
    }catch(ArrayIndexOutOfBoundsException e){  
       System.out.println("Exception thrown  :" + e);  
    }  
    finally{  
       a[0] = 6;  
       System.out.println("First element value: " +a[0]);  
       System.out.println("The finally statement is executed");  
    }  
  }  
}  
```  
catch 不能独立于 try 存在。  
在 try/catch 后面添加 finally 块并非强制性要求的。  
try 代码后不能既没 catch 块也没 finally 块。  
try, catch, finally 块之间不能添加任何代码。  
  
声明自定义异常  
在 Java 中你可以自定义异常。编写自己的异常类时需要记住下面的几点。  
所有异常都必须是 Throwable 的子类。  
如果希望写一个检查性异常类，则需要继承 Exception 类。  
如果你想写一个运行时异常类，那么需要继承 RuntimeException 类。  
只继承Exception 类来创建的异常类是检查性异常类。  
  
通用异常  
在Java中定义了两种类型的异常和错误。  
JVM(Java虚拟机) 异常：由 JVM 抛出的异常或错误。例如：NullPointerException 类，ArrayIndexOutOfBoundsException 类，ClassCastException 类。  
程序级异常：由程序或者API程序抛出的异常。例如 IllegalArgumentException 类，IllegalStateException 类。  
  
Java 继承  
继承是java面向对象编程技术的一块基石，因为它允许创建分等级层次的类。  
继承就是子类继承父类的特征和行为，使得子类对象（实例）具有父类的实例域和方法，或子类从父类继承方法，使得子类具有父类相同的行为。  
类的继承格式  
在 Java 中通过 extends 关键字可以申明一个类是从另外一个类继承而来的，一般形式如下：  
类的继承格式  
class 父类 {  
}  
class 子类 extends 父类 {  
}  
Java 不支持多继承，但支持多重继承。  
  
继承的特性  
子类拥有父类非 private 的属性、方法。  
子类可以拥有自己的属性和方法，即子类可以对父类进行扩展。  
子类可以用自己的方式实现父类的方法。  
Java 的继承是单继承，但是可以多重继承，单继承就是一个子类只能继承一个父类，多重继承就是，例如 A 类继承 B 类，B 类继承 C 类，所以按照关系就是 C 类是 B 类的父类，B 类是 A 类的父类，这是 Java 继承区别于 C++ 继承的一个特性。  
提高了类之间的耦合性（继承的缺点，耦合度高就会造成代码之间的联系越紧密，代码独立性越差）。  
  
继承关键字  
继承可以使用 extends 和 implements 这两个关键字来实现继承，而且所有的类都是继承于 java.lang.Object，当一个类没有继承的两个关键字，则默认继承object（这个类在 java.lang 包中，所以不需要 import）祖先类。  
extends关键字  
在 Java 中，类的继承是单一继承，也就是说，一个子类只能拥有一个父类，所以 extends 只能继承一个类。  
implements关键字  
使用 implements 关键字可以变相的使java具有多继承的特性，使用范围为类继承接口的情况，可以同时继承多个接口（接口跟接口之间采用逗号分隔）。  
```  
public interface A {  
    public void eat();  
    public void sleep();  
}  
public interface B {  
    public void show();  
}  
public class C implements A,B {  
}  
```  
  
super 与 this 关键字  
super关键字：我们可以通过super关键字来实现对父类成员的访问，用来引用当前对象的父类。  
this关键字：指向自己的引用。  
  
final关键字  
final 关键字声明类可以把类定义为不能继承的，即最终类；或者用于修饰方法，该方法不能被子类重写：  
声明类：  
final class 类名 {//类体}  
声明方法：  
修饰符(public/private/default/protected) final 返回值类型 方法名(){//方法体}  
  
构造器  
子类是不继承父类的构造器（构造方法或者构造函数）的，它只是调用（隐式或显式）。如果父类的构造器带有参数，则必须在子类的构造器中显式地通过 super 关键字调用父类的构造器并配以适当的参数列表。  
如果父类构造器没有参数，则在子类的构造器中不需要使用 super 关键字调用父类构造器，系统会自动调用父类的无参构造器。  
  
Java 重写(Override)与重载(Overload)  
重写(Override)  
重写是子类对父类的允许访问的方法的实现过程进行重新编写, 返回值和形参都不能改变。即外壳不变，核心重写！  
重写的好处在于子类可以根据需要，定义特定于自己的行为。 也就是说子类能够根据需要实现父类的方法。  
重写方法不能抛出新的检查异常或者比被重写方法申明更加宽泛的异常。例如： 父类的一个方法申明了一个检查异常 IOException，但是在重写这个方法的时候不能抛出 Exception 异常，因为 Exception 是 IOException 的父类，只能抛出 IOException 的子类异常。  
在面向对象原则里，重写意味着可以重写任何现有方法。  
  
方法的重写规则  
参数列表必须完全与被重写方法的相同。  
返回类型与被重写方法的返回类型可以不相同，但是必须是父类返回值的派生类（java5 及更早版本返回类型要一样，java7 及更高版本可以不同）。  
访问权限不能比父类中被重写的方法的访问权限更低。例如：如果父类的一个方法被声明为 public，那么在子类中重写该方法就不能声明为 protected。  
父类的成员方法只能被它的子类重写。  
声明为 final 的方法不能被重写。  
声明为 static 的方法不能被重写，但是能够被再次声明。  
子类和父类在同一个包中，那么子类可以重写父类所有方法，除了声明为 private 和 final 的方法。  
子类和父类不在同一个包中，那么子类只能够重写父类的声明为 public 和 protected 的非 final 方法。  
重写的方法能够抛出任何非强制异常，无论被重写的方法是否抛出异常。但是，重写的方法不能抛出新的强制性异常，或者比被重写方法声明的更广泛的强制性异常，反之则可以。  
构造方法不能被重写。  
如果不能继承一个方法，则不能重写这个方法。  
  
重载(Overload)  
重载(overloading) 是在一个类里面，方法名字相同，而参数不同。返回类型可以相同也可以不同。  
每个重载的方法（或者构造函数）都必须有一个独一无二的参数类型列表。  
最常用的地方就是构造器的重载。  
重载规则:  
被重载的方法必须改变参数列表(参数个数或类型不一样)；  
被重载的方法可以改变返回类型；  
被重载的方法可以改变访问修饰符；  
被重载的方法可以声明新的或更广的检查异常；  
方法能够在同一个类中或者在一个子类中被重载。  
无法以返回值类型作为重载函数的区分标准。  
  
重写与重载之间的区别  
区别点 重载方法  重写方法  
参数列表  必须修改  一定不能修改  
返回类型  可以修改  一定不能修改  
异常  可以修改  可以减少或删除，一定不能抛出新的或者更广的异常  
访问  可以修改  一定不能做更严格的限制（可以降低限制）  
方法的重写(Overriding)和重载(Overloading)是java多态性的不同表现，重写是父类与子类之间多态性的一种表现，重载可以理解成多态的具体表现形式。  
(1)方法重载是一个类中定义了多个方法名相同,而他们的参数的数量不同或数量相同而类型和次序不同,则称为方法的重载(Overloading)。  
(2)方法重写是在子类存在方法与父类的方法的名字相同,而且参数的个数与类型一样,返回值也一样的方法,就称为重写(Overriding)。  
(3)方法重载是一个类的多态性表现,而方法重写是子类与父类的一种多态性表现。  
  
Java 多态  
多态是同一个行为具有多个不同表现形式或形态的能力。  
多态就是同一个接口，使用不同的实例而执行不同操作。  
多态存在的三个必要条件: 继承,重写,父类引用指向子类对象  
比如：  
Parent p = new Child();  
当使用多态方式调用方法时，首先检查父类中是否有该方法，如果没有，则编译错误；如果有，再去调用子类的同名方法。  
多态的好处：可以使程序有良好的扩展，并可以对所有类的对象进行通用处理。  
```  
public class Test {  
    public static void main(String[] args) {  
        show(new Cat());  // 以 Cat 对象调用 show 方法  
        show(new Dog());  // 以 Dog 对象调用 show 方法  
        Animal a = new Cat();  // 向上转型  
        a.eat();               // 调用的是 Cat 的 eat  
        Cat c = (Cat)a;        // 向下转型  
        c.work();        // 调用的是 Cat 的 work  
    }  
    public static void show(Animal a)  {  
        a.eat();  
        // 类型判断  
        if (a instanceof Cat)  {  // 猫做的事情  
            Cat c = (Cat)a;  
            c.work();  
        } else if (a instanceof Dog) { // 狗做的事情  
            Dog c = (Dog)a;  
            c.work();  
        }  
    }  
}  
abstract class Animal {  
    abstract void eat();  
}  
class Cat extends Animal {  
    public void eat() {  
        System.out.println("吃鱼");  
    }  
    public void work() {  
        System.out.println("抓老鼠");  
    }  
}  
class Dog extends Animal {  
    public void eat() {  
        System.out.println("吃骨头");  
    }  
    public void work() {  
        System.out.println("看家");  
    }  
}  
```  
  
虚函数  
虚函数的存在是为了多态。  
Java 中其实没有虚函数的概念，它的普通函数就相当于 C++ 的虚函数，动态绑定是Java的默认行为。如果 Java 中不希望某个函数具有虚函数特性，可以加上 final 关键字变成非虚函数。  
  
Java 抽象类  
在面向对象的概念中，所有的对象都是通过类来描绘的，但是反过来，并不是所有的类都是用来描绘对象的，如果一个类中没有包含足够的信息来描绘一个具体的对象，这样的类就是抽象类。  
抽象类除了不能实例化对象之外，类的其它功能依然存在，成员变量、成员方法和构造方法的访问方式和普通类一样。  
由于抽象类不能实例化对象，所以抽象类必须被继承，才能被使用。也是因为这个原因，通常在设计阶段决定要不要设计抽象类。  
父类包含了子类集合的常见的方法，但是由于父类本身是抽象的，所以不能使用这些方法。  
在Java中抽象类表示的是一种继承关系，一个类只能继承一个抽象类，而一个类却可以实现多个接口。  
  
抽象方法  
如果你想设计这样一个类，该类包含一个特别的成员方法，该方法的具体实现由它的子类确定，那么你可以在父类中声明该方法为抽象方法。  
Abstract 关键字同样可以用来声明抽象方法，抽象方法只包含一个方法名，而没有方法体。  
抽象方法没有定义，方法名后面直接跟一个分号，而不是花括号。  
声明抽象方法会造成以下两个结果：  
如果一个类包含抽象方法，那么该类必须是抽象类。  
任何子类必须重写父类的抽象方法，或者声明自身为抽象类。  
  
Java 封装  
在面向对象程式设计方法中，封装（英语：Encapsulation）是指一种将抽象性函式接口的实现细节部份包装、隐藏起来的方法。  
封装可以被认为是一个保护屏障，防止该类的代码和数据被外部类定义的代码随机访问。  
要访问该类的代码和数据，必须通过严格的接口控制。  
封装最主要的功能在于我们能修改自己的实现代码，而不用修改那些调用我们代码的程序片段。  
适当的封装可以让程式码更容易理解与维护，也加强了程式码的安全性。  
封装的优点  
1. 良好的封装能够减少耦合。  
2. 类内部的结构可以自由修改。  
3. 可以对成员变量进行更精确的控制。  
4. 隐藏信息，实现细节。  
  
实现Java封装的步骤  
1. 修改属性的可见性来限制对属性的访问（一般限制为private），例如：  
public class Person {  
    private String name;  
    private int age;  
}  
这段代码中，将 name 和 age 属性设置为私有的，只能本类才能访问，其他类都访问不了，如此就对信息进行了隐藏。  
2. 对每个值属性提供对外的公共方法访问，也就是创建一对赋取值方法，用于对私有属性的访问，例如：  
public class Person{  
    private String name;  
    private int age;  
    public int getAge(){  
      return age;  
    }  
    public String getName(){  
      return name;  
    }  
    public void setAge(int age){  
      this.age = age;  
    }  
    public void setName(String name){  
      this.name = name;  
    }  
}  
采用 this 关键字是为了解决实例变量（private String name）和局部变量（setName(String name)中的name变量）之间发生的同名的冲突。  
  
  
Java 接口  
接口（英文：Interface），在JAVA编程语言中是一个抽象类型，是抽象方法的集合，接口通常以interface来声明。一个类通过继承接口的方式，从而来继承接口的抽象方法。  
接口并不是类，编写接口的方式和类很相似，但是它们属于不同的概念。类描述对象的属性和方法。接口则包含类要实现的方法。  
除非实现接口的类是抽象类，否则该类要定义接口中的所有方法。  
接口无法被实例化，但是可以被实现。一个实现接口的类，必须实现接口内所描述的所有方法，否则就必须声明为抽象类。另外，在 Java 中，接口类型可用来声明一个变量，他们可以成为一个空指针，或是被绑定在一个以此接口实现的对象。  
  
接口与类相似点：  
一个接口可以有多个方法。  
接口文件保存在 .java 结尾的文件中，文件名使用接口名。  
接口的字节码文件保存在 .class 结尾的文件中。  
接口相应的字节码文件必须在与包名称相匹配的目录结构中。  
接口与类的区别：  
接口不能用于实例化对象。  
接口没有构造方法。  
接口中所有的方法必须是抽象方法。  
接口不能包含成员变量，除了 static 和 final 变量。  
接口不是被类继承了，而是要被类实现。  
接口支持多继承。  
抽象类和接口的区别  
1. 抽象类中的方法可以有方法体，就是能实现方法的具体功能，但是接口中的方法不行。  
2. 抽象类中的成员变量可以是各种类型的，而接口中的成员变量只能是 public static final 类型的。  
3. 一个类只能继承一个抽象类，而一个类却可以实现多个接口。  
  
接口特性  
接口中的方法都是公有的。  
接口是隐式抽象的，当声明一个接口的时候，不必使用abstract关键字。  
接口中每一个方法也是隐式抽象的，声明时同样不需要abstract关键字。接口中的方法会被隐式的指定为 public abstract（只能是 public abstract，其他修饰符都会报错）。  
接口中可以含有变量，但是接口中的变量会被隐式的指定为 public static final 变量（并且只能是 public，用 private 修饰会报编译错误）。  
接口中的方法是不能在接口中实现的，只能由实现接口的类来实现接口中的方法。  
  
接口的声明  
接口的声明语法格式如下：  
[可见度] interface 接口名称 [extends 其他的接口名] {  
        // 声明变量  
        // 抽象方法  
}  
Interface关键字用来声明一个接口。下面是接口声明的一个简单例子。  
  
接口的实现  
当类实现接口的时候，类要实现接口中所有的方法。否则，类必须声明为抽象的类。  
类使用implements关键字实现接口。在类声明中，Implements关键字放在class声明后面。  
实现一个接口的语法，可以使用这个公式：  
...implements 接口名称[, 其他接口名称, 其他接口名称..., ...] ...  
重写接口中声明的方法时，需要注意以下规则：  
类在实现接口的方法时，不能抛出强制性异常，只能在接口中，或者继承接口的抽象类中抛出该强制性异常。  
类在重写方法时要保持一致的方法名，并且应该保持相同或者相兼容的返回值类型。  
如果实现接口的类是抽象类，那么就没必要实现该接口的方法。  
在实现接口的时候，也要注意一些规则：  
一个类可以同时实现多个接口。  
一个类只能继承一个类，但是能实现多个接口。  
一个接口能继承另一个接口，这和类之间的继承比较相似。  
  
接口的继承  
一个接口能继承另一个接口，和类之间的继承方式比较相似。接口的继承使用extends关键字，子接口继承父接口的方法。  
接口的多继承  
在Java中，类的多继承是不合法，但接口允许多继承。  
在接口的多继承中extends关键字只需要使用一次，在其后跟着继承接口。 如下所示：  
public interface Hockey extends Sports, Event  
以上的程序片段是合法定义的子接口，与类不同的是，接口允许多继承，而 Sports及 Event 可能定义或是继承相同的方法  
  
标记接口  
最常用的继承接口是没有包含任何方法的接口。  
标记接口是没有任何方法和属性的接口.它仅仅表明它的类属于一个特定的类型,供其他代码来测试允许做一些事情。  
标记接口作用：简单形象的说就是给某个对象打个标（盖个戳），使对象拥有某个或某些特权。  
标记接口主要用于以下两种目的：  
建立一个公共的父接口：  
正如EventListener接口，这是由几十个其他接口扩展的Java API，你可以使用一个标记接口来建立一组接口的父接口。例如：当一个接口继承了EventListener接口，Java虚拟机(JVM)就知道该接口将要被用于一个事件的代理方案。  
向一个类添加数据类型：  
这种情况是标记接口最初的目的，实现标记接口的类不需要定义任何接口方法(因为标记接口根本就没有方法)，但是该类通过多态性变成一个接口类型。  
  
Java 包(package)  
为了更好地组织类，Java 提供了包机制，用于区别类名的命名空间。  
包的作用  
1、把功能相似或相关的类或接口组织在同一个包中，方便类的查找和使用。  
2、如同文件夹一样，包也采用了树形目录的存储方式。同一个包中的类名字是不同的，不同的包中的类的名字是可以相同的，当同时调用两个不同包中相同类名的类时，应该加上包名加以区别。因此，包可以避免名字冲突。  
3、包也限定了访问权限，拥有包访问权限的类才能访问某个包中的类。  
Java 使用包（package）这种机制是为了防止命名冲突，访问控制，提供搜索和定位类（class）、接口、枚举（enumerations）和注释（annotation）等。  
包语句的语法格式为：  
package pkg1[．pkg2[．pkg3…]];  
例如,一个Something.java 文件它的内容  
package net.java.util;  
public class Something{  
   ...  
}  
那么它的路径应该是 net/java/util/Something.java 这样保存的。 package(包) 的作用是把不同的 java 程序分类保存，更方便的被其他 java 程序调用。  
一个包（package）可以定义为一组相互联系的类型（类、接口、枚举和注释），为这些类型提供访问保护和命名空间管理的功能。  
以下是一些 Java 中的包：  
java.lang-打包基础的类  
java.io-包含输入输出功能的函数  
由于包创建了新的命名空间（namespace），所以不会跟其他包中的任何名字产生命名冲突。使用包这种机制，更容易实现访问控制，并且让定位相关类更加简单。  
  
创建包  
创建包的时候，你需要为这个包取一个合适的名字。之后，如果其他的一个源文件包含了这个包提供的类、接口、枚举或者注释类型的时候，都必须将这个包的声明放在这个源文件的开头。  
包声明应该在源文件的第一行，每个源文件只能有一个包声明，这个文件中的每个类型都应用于它。  
如果一个源文件中没有使用包声明，那么其中的类，函数，枚举，注释等将被放在一个无名的包（unnamed package）中。  
  
import 关键字  
为了能够使用某一个包的成员，我们需要在 Java 程序中明确导入该包。使用 "import" 语句可完成此功能。  
在 java 源文件中 import 语句应位于 package 语句之后，所有类的定义之前，可以没有，也可以有多条，其语法格式为：  
import package1[.package2…].(classname|\*);  
如果在一个包中，一个类想要使用本包中的另一个类，那么该包名可以省略。  
类文件中可以包含任意数量的 import 声明。import 声明必须在包声明之后，类声明之前。  
  
package 的目录结构  
类放在包中会有两种主要的结果：  
包名成为类名的一部分，正如我们前面讨论的一样。  
包名必须与相应的字节码所在的目录结构相吻合。  
通常，一个公司使用它互联网域名的颠倒形式来作为它的包名.例如：互联网域名是 runoob.com，所有的包名都以 com.runoob 开头。包名中的每一个部分对应一个子目录。  
例如：有一个 com.runoob.test 的包，这个包包含一个叫做 Runoob.java 的源文件，那么相应的，应该有如下面的一连串子目录：  
....\com\runoob\test\Runoob.java  
编译的时候，编译器为包中定义的每个类、接口等类型各创建一个不同的输出文件，输出文件的名字就是这个类型的名字，并加上 .class 作为扩展后缀。  
  
Java 泛型  
Java 泛型（generics）提供了编译时类型安全检测机制，该机制允许程序员在编译时检测到非法的类型。泛型的本质是参数化类型，也就是说所操作的数据类型被指定为一个参数。  
泛型方法  
你可以写一个泛型方法，该方法在调用时可以接收不同类型的参数。根据传递给泛型方法的参数类型，编译器适当地处理每一个方法调用。  
下面是定义泛型方法的规则：  
所有泛型方法声明都有一个类型参数声明部分（由尖括号分隔），该类型参数声明部分在方法返回类型之前（在下面例子中的<E>）。  
每一个类型参数声明部分包含一个或多个类型参数，参数间用逗号隔开。一个泛型参数，也被称为一个类型变量，是用于指定一个泛型类型名称的标识符。  
类型参数能被用来声明返回值类型，并且能作为泛型方法得到的实际参数类型的占位符。  
泛型方法体的声明和其他方法一样。注意类型参数只能代表引用型类型，不能是原始类型（像int,double,char的等）。  
```  
public class GenericMethodTest {  
  // 泛型方法 printArray  
  public static <E> void printArray(E[] inputArray) {  
    // 输出数组元素  
    for (E element : inputArray) {  
      System.out.printf("%s ", element);  
    }  
    System.out.println();  
  }  
  public static void main(String args[]) {  
    // 创建不同类型数组： Integer, Double 和 Character  
    Integer[] intArray = {1, 2, 3, 4, 5};  
    Double[] doubleArray = {1.1, 2.2, 3.3, 4.4};  
    Character[] charArray = {'H', 'E', 'L', 'L', 'O'};  
    System.out.println("整型数组元素为:");  
    printArray(intArray); // 传递一个整型数组  
    System.out.println("\n双精度型数组元素为:");  
    printArray(doubleArray); // 传递一个双精度型数组  
    System.out.println("\n字符型数组元素为:");  
    printArray(charArray); // 传递一个字符型数组  
  }  
}  
```  
  
有界的类型参数:  
可能有时候，你会想限制那些被允许传递到一个类型参数的类型种类范围。例如，一个操作数字的方法可能只希望接受Number或者Number子类的实例。这就是有界类型参数的目的。  
要声明一个有界的类型参数，首先列出类型参数的名称，后跟extends关键字，最后紧跟它的上界。  
下面的例子演示了"extends"如何使用在一般意义上的意思"extends"（类）或者"implements"（接口）。该例子中的泛型方法返回三个可比较对象的最大值。  
```  
public class MaximumTest {  
  // 比较三个值并返回最大值  
  public static <T extends Comparable<T>> T maximum(T x, T y, T z) {  
    T max = x; // 假设x是初始最大值  
    if (y.compareTo(max) > 0) {  
      max = y; // y 更大  
    }  
    if (z.compareTo(max) > 0) {  
      max = z; // 现在 z 更大  
    }  
    return max; // 返回最大对象  
  }  
  public static void main(String args[]) {  
    System.out.printf("%d, %d 和 %d 中最大的数为 %d\n\n", 3, 4, 5, maximum(3, 4, 5));  
    System.out.printf("%.1f, %.1f 和 %.1f 中最大的数为 %.1f\n\n", 6.6, 8.8, 7.7, maximum(6.6, 8.8, 7.7));  
    System.out.printf(  
        "%s, %s 和 %s 中最大的数为 %s\n", "pear", "apple", "orange", maximum("pear", "apple", "orange"));  
  }  
}  
```  
  
泛型类  
泛型类的声明和非泛型类的声明类似，除了在类名后面添加了类型参数声明部分。  
和泛型方法一样，泛型类的类型参数声明部分也包含一个或多个类型参数，参数间用逗号隔开。一个泛型参数，也被称为一个类型变量，是用于指定一个泛型类型名称的标识符。因为他们接受一个或多个参数，这些类被称为参数化的类或参数化的类型。  
如下实例演示了我们如何定义一个泛型类:  
```  
public class Box<T> {  
  private T t;  
  public void add(T t) {  
    this.t = t;  
  }  
  public T get() {  
    return t;  
  }  
  public static void main(String[] args) {  
    Box<Integer> integerBox = new Box<Integer>();  
    Box<String> stringBox = new Box<String>();  
    integerBox.add(new Integer(10));  
    stringBox.add(new String("菜鸟教程"));  
    System.out.printf("整型值为 :%d\n\n", integerBox.get());  
    System.out.printf("字符串为 :%s\n", stringBox.get());  
  }  
}  
```  
  
类型通配符  
1、类型通配符一般是使用?代替具体的类型参数。例如 List<?> 在逻辑上是List<String>,List<Integer> 等所有List<具体类型实参>的父类。  
```  
import java.util.*;  
public class GenericTest {  
    public static void main(String[] args) {  
        List<String> name = new ArrayList<String>();  
        List<Integer> age = new ArrayList<Integer>();  
        List<Number> number = new ArrayList<Number>();  
        name.add("icon");  
        age.add(18);  
        number.add(314);  
        getData(name);  
        getData(age);  
        getData(number);  
   }  
   public static void getData(List<?> data) {  
      System.out.println("data :" + data.get(0));  
   }  
}  
```  
因为getData()方法的参数是List类型的，所以name，age，number都可以作为这个方法的实参，这就是通配符的作用。  
2、类型通配符上限通过形如List来定义，如此定义就是通配符泛型值接受Number及其下层子类类型。  
```  
import java.util.*;  
public class GenericTest {  
    public static void main(String[] args) {  
        List<String> name = new ArrayList<String>();  
        List<Integer> age = new ArrayList<Integer>();  
        List<Number> number = new ArrayList<Number>();  
        name.add("icon");  
        age.add(18);  
        number.add(314);  
        //getUperNumber(name);//1  
        getUperNumber(age);//2  
        getUperNumber(number);//3  
   }  
   public static void getData(List<?> data) {  
      System.out.println("data :" + data.get(0));  
   }  
   public static void getUperNumber(List<? extends Number> data) {  
          System.out.println("data :" + data.get(0));  
   }  
}  
```  
3、类型通配符下限通过形如 List<? super Number>来定义，表示类型只能接受Number及其三层父类类型，如 Object 类型的实例。  
  
Java 序列化  
Java 提供了一种对象序列化的机制，该机制中，一个对象可以被表示为一个字节序列，该字节序列包括该对象的数据、有关对象的类型的信息和存储在对象中数据的类型。  
将序列化对象写入文件之后，可以从文件中读取出来，并且对它进行反序列化，也就是说，对象的类型信息、对象的数据，还有对象中的数据类型可以用来在内存中新建对象。  
整个过程都是 Java 虚拟机（JVM）独立的，也就是说，在一个平台上序列化的对象可以在另一个完全不同的平台上反序列化该对象。  
类 ObjectInputStream 和 ObjectOutputStream 是高层次的数据流，它们包含反序列化和序列化对象的方法。  
一个类的对象要想序列化成功，必须满足两个条件：  
该类必须实现 java.io.Serializable 接口。  
该类的所有属性必须是可序列化的。如果有一个属性不是可序列化的，则该属性必须注明是短暂的。  
如果你想知道一个 Java 标准类是否是可序列化的，请查看该类的文档。检验一个类的实例是否能序列化十分简单， 只需要查看该类有没有实现 java.io.Serializable接口。  
```  
public class Employee implements java.io.Serializable  
{  
   public String name;  
   public String address;  
   public transient int SSN;  
   public int number;  
   public void mailCheck()  
   {  
      System.out.println("Mailing a check to " + name  
                           + " " + address);  
   }  
}  
```  
  
序列化对象  
ObjectOutputStream 类用来序列化一个对象，如下的 SerializeDemo 例子实例化了一个 Employee 对象，并将该对象序列化到一个文件中。  
该程序执行后，就创建了一个名为 employee.ser 文件。该程序没有任何输出，但是你可以通过代码研读来理解程序的作用。  
注意： 当序列化一个对象到文件时， 按照 Java 的标准约定是给文件一个 .ser 扩展名。  
SerializeDemo.java 文件代码：  
```  
import java.io.*;  
public class SerializeDemo  
{  
   public static void main(String [] args)  
   {  
      Employee e = new Employee();  
      e.name = "Reyan Ali";  
      e.address = "Phokka Kuan, Ambehta Peer";  
      e.SSN = 11122333;  
      e.number = 101;  
      try  
      {  
         FileOutputStream fileOut =  
         new FileOutputStream("/tmp/employee.ser");  
         ObjectOutputStream out = new ObjectOutputStream(fileOut);  
         out.writeObject(e);  
         out.close();  
         fileOut.close();  
         System.out.printf("Serialized data is saved in /tmp/employee.ser");  
      }catch(IOException i)  
      {  
          i.printStackTrace();  
      }  
   }  
}  
```  
  
反序列化对象  
下面的 DeserializeDemo 程序实例了反序列化，/tmp/employee.ser 存储了 Employee 对象。  
DeserializeDemo.java 文件代码：  
```  
import java.io.*;  
public class DeserializeDemo  
{  
   public static void main(String [] args)  
   {  
      Employee e = null;  
      try  
      {  
         FileInputStream fileIn = new FileInputStream("/tmp/employee.ser");  
         ObjectInputStream in = new ObjectInputStream(fileIn);  
         e = (Employee) in.readObject();  
         in.close();  
         fileIn.close();  
      }catch(IOException i)  
      {  
         i.printStackTrace();  
         return;  
      }catch(ClassNotFoundException c)  
      {  
         System.out.println("Employee class not found");  
         c.printStackTrace();  
         return;  
      }  
      System.out.println("Deserialized Employee...");  
      System.out.println("Name: " + e.name);  
      System.out.println("Address: " + e.address);  
      System.out.println("SSN: " + e.SSN);  
      System.out.println("Number: " + e.number);  
    }  
}  
```  
readObject() 方法中的 try/catch代码块尝试捕获 ClassNotFoundException 异常。对于 JVM 可以反序列化对象，它必须是能够找到字节码的类。如果JVM在反序列化对象的过程中找不到该类，则抛出一个 ClassNotFoundException 异常。  
注意，readObject() 方法的返回值被转化成 Employee 引用。  
当对象被序列化时，属性 SSN 的值为 111222333，但是因为该属性是短暂的，该值没有被发送到输出流。所以反序列化后 Employee 对象的 SSN 属性为 0。  
