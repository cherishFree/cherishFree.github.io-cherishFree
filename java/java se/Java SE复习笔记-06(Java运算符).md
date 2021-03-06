# Java SE复习笔记-06
## Java 运算符
计算机最基本的用途之一就是执行数学运算，作为一门计算机语言，Java也提供了一套丰富的运算符来操纵变量。我们可以把运算符分成以下几组：
- 算数运算符
- 关系运算符
- 位运算符
- 逻辑运算符
- 赋值运算符
- 其他运算符


#### 算数运算符  
算数运算符用在数学表达式中，它们的作用和数学中的作用一样。  
*表格中的实例假设整数变量A的值为10，B的值为20*
操作符|描述|例子
---|---|---|
\+ | 加法\-相加运算符两侧的值|A\+B=30
\- | 减法\-左操作数减去右操作数 | A\-B=10
\* | 乘法\-相乘操作符两侧的值|A*B=200
\/ | 除法\-左操作数除以右操作数|B\/A=2
\% | 取余\-左操作数除以右操作数的余数|B\%A=0
\++ | 自增：操作数加1 | B++或者++B等于21
\-- | 自减：操作数减少1 | B--或者--B等于19

**自增自减运算符**  
1、自增自减运算符是一种特殊的算数运算符，在算数运算符中需要两个操作数来进行运算，而自增自减运算是一个操作数。  
2、前缀自增自减法(++a,--a)：先进行自增自减运算，再进行表达式运算。  
3、后缀自增自减法(a++,a--)：先进行表达式运算再进行自增或自减运算。   
`public class selfAddMinus{
    public static void main(String[] args){
        int a = 5;
        int b = 5;
        int x = 2*++a;
        int y = 2*b++;
        System.out.println("a="+a+",x="+x);
        System.out.println("b="+b+",y="+y);
    }
}` 

#### 关系运算符  
*表格中的实例整数变量A为10，B为20*  
运算符 | 描述 | 例子
---|---|---|
== | 检查如果两个操作数的值相等，如果相等则条件为真 | (A==B)为假
!= | 检查如果两个操作数的值是否相等，如果值不相等则条件为真 | (A != B)为真
\> | 检查左操作数的值是否大于右操作数的值，如果是那么条件为真 | (A>B) 为假
< | 检查左操作数的值是否小于右操作数的值，如果是那么条件为真 | (A<B) 为真
\>= | 检查左操作数的值是否大于或者等于右操作数的值，如果是那么条件为真 | (A >= B )为假
<= | 检查左操作数的值是否小于或者等于右操作数的值，如果是那么条件为真 | (A <= B )为真

#### 位运算符
Java定义了位运算符，应用于整数类型(int)、长整型(long)、短整型(short)、字符型(char)和字节型(byte)等类型。  
位运算符作用在所有的位上，并且按位运算。  
*下面表格中的整数变量A的值为60，B的值为13*
操作符|描述|例子
---|---|---|
& | 如果相对应的位都是1，则结果为1，否则为0 | (A & B ),得到为12，即0000 1100
\| | 如果对应位都是0，则结果为0，否则为1 | (A \|B )得到61，即0011 1101
^ | 如果对应位值相同，则结果为0，否则为1 | (A ^ B )0011 0001
~ | 按位取反操作符，翻转操作数的每一位，即0变1,1变0 | (~A)得到-61，即1100 0011
<< | 按位左移运算符，左操作数按位左移右操作数指定的位数 | A<<240 即1111 0000 
\>> | 按位右移运算符。左操作数按位右移右操作数指定的位数 | A\>>2得15 1111
\>>> | 按位右移补零操作符。左操作数的值按右操作数指定的位数右移，移动得到的空位以零填充 | A \>>>2 得到15，即0000 1111

#### 逻辑运算符 
*下表中布尔变量A值为真，B值为假*  
操作符 | 描述 | 例子
---|---|---|
&& | 称为逻辑与运算，当且仅当两个操作数都为真，条件才为真 | (A && B) 为假
\|\| | 称为逻辑或操作符，如果任何两个操作数任何一个为真，条件为真 | (A \|\|B) 为真
! | 称为逻辑非运算符，用来翻转操作数的逻辑状态，如果条件为true，则逻辑非运算符将得到false | !(A && B) 为真


#### 赋值运算符  

操作符 | 描述 | 例子
---|---|---|
=	|简单的赋值运算符，将右操作数的值赋给左侧操作数|	C = A + B将把A + B得到的值赋给C
+=	|加和赋值操作符，它把左操作数和右操作数相加赋值给左操作数	|C += A等价于C = C + A
-=	|减和赋值操作符，它把左操作数和右操作数相减赋值给左操作数	|C -= A等价于C = C - A
*=	|乘和赋值操作符，它把左操作数和右操作数相乘赋值给左操作数	|C *= A等价于C = C * A
/ =	|除和赋值操作符，它把左操作数和右操作数相除赋值给左操作数	|C /= A，C 与 A 同类型时等价于 C = C / A
(％)=	|取模和赋值操作符，它把左操作数和右操作数取模后赋值给左操作数	|C %= A等价于C = C ％ A
<<=	|左移位赋值运算符	|C <<= 2等价于C = C << 2
\>\>=	|右移位赋值运算符	|C \>\>= 2等价于C = C \>\> 2
&=	|按位与赋值运算符	|C &= 2等价于C = C＆2
^=	|按位异或赋值操作符	|C ^= 2等价于C = C ^ 2
\|=	|按位或赋值操作符	|C \|= 2等价于C = C \| 2


#### 条件运算符  
条件运算符也被称为三目运算符，该运算符有3个操作数，并且需要判断布尔表达式的值。该运算符主要是决定哪个值应该赋值给变量。  
`variable x = (expression) ? value if true : value if false`  


#### instanceof运算符
该运算符用于操作对象实例，检查该对象是否是一个特定类型（类类型或者接口类型）。  
`(Object reference variable) instanceof (class/interface type)`  


#### Java 运算符优先级  

类别 | 操作符 | 关联性 
---| ---| ---|
后缀|() [] . (点操作符)	|左到右
一元|	++ -- + - ～ ！	|从右到左
乘性 |	* /％	|左到右
加性 |	+ -	|左到右
移位 |	\>\> &ensp;\>\>\> &ensp; << 	|左到右
关系 |	\>\>= &ensp; <<= 	|左到右
相等 |	== &ensp; !=	|左到右
按位与|	＆	|左到右
按位异或|	^	|左到右
按位或|	\|	|左到右
逻辑与|	&&	|左到右
逻辑或|	\|\|	|左到右
条件|	？：	|从右到左
赋值|	= &ensp;+= &ensp;-= &ensp;*= &ensp;/=&ensp;％= &ensp;\>\>= &ensp;<<=&ensp;＆= &ensp;^=&ensp; \|=	|从右到左
逗号|	,|	左到右
