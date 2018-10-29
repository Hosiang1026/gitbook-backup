# 基础语法

## 一、规范

**标识符：**凡是自己命名的地方都叫标识符。 

    如： 包名、类名、接口名、方法名、变量名、常量名

**关键字：**被Java赋予了特殊含义的单词。

### 1.1 命名的规则 

①可使用 字母  A-Z  a-z  数字 0-9   特殊字符  下划线 "_" 和  美元符 “$”

②数字不能开头

③其中不能包含空格

④不能使用关键字和保留字，但是可以包含关键字和保留字

⑤Java严格区分大小写，但是长度无限制。

    注：必须遵守，若不遵守编译不能通过

### 1.2 命名的规范 

①包名： 所有字母都小写。 如： xxxyyyzzz

②类名、接口名：若出现多个单词，每个单词首字母都大写。如： XxxYyyZzz

③方法名、变量名： 若出现多个单词，第一个单词的首字母小写，其余单词首字母都大写。如： xxxYyyZzz

④常量名： 所有字母都大写，每个单词之间以 "_" 分隔。 如： XXX_YYY_ZZZ

    注：可以不遵守，但是会收到鄙视

## 二、变量

变量：用于保存数据

局部变量  &  成员变量
1. 变量的格式：   数据类型   变量名   =   值;
    //声明一个变量
    数据类型  变量名;    如:  int var;
    //为变量赋值
    变量名 =  值；    如： var = 10;
    //声明一个变量并赋值
    int var = 10;

2. 变量的概念：
    ①在内存中开辟一块内存空间
    ②该空间有名称（变量名）有类型（数据类型）
    ③变量可以在指定的范围内不断的变化

3. 变量的注意：
    ①作用域：变量作用在所属的那对 {}  内
    ②局部变量在使用前必须赋初始值
    ③先声明，后使用

## 三、进制之间的转换（了解）

## 四、变量的数据类型

基本数据类型（8种）：

    整型： byte(8位)  short(16位)  int(32位)-默认类型 long(64位)

    浮点型： float(32位)  double(64位)---默认类型

    字符型： char(2个字节---16位)

    布尔型： boolean

引用数据类型：

    |---类(class)   --------------------  String 字符串

    |---接口(interface)

    |---数组([])

声明变量的注意：

    ①声明 long 型变量，值后需要加 L 或 l .  如：  long l = 123456l;    long l1 = 123456L;
   
    ②声明 float 型变量，值后必须加 F 或 f 。 如： float f = 15.6f;
    
    ③声明 double 型变量，值后可以加 D 或 d 。  如： double d1 = 167.7D;
    
    ④声明 char 型变量，值必须使用单引号。只能存储单个字符
       存储 Unicode 编码（ASCII 、 中文、日文、特殊字符等等）

    ⑤声明 String 变量，值必须使用双引号

## 五、变量的运算

数据类型的转换：

自动类型转换（自动升级）：小容量转大容量。（系统自动完成）

    ①byte  short  char   --->   int  --->  long  ---> float  --->  double

    ②byte short  char  三者之间不进行运算，若运算自动提升成 int 再做运算
            char c1 = 'A';
            char c2 = 'B';
            int i = c1 + c2;

    ③boolean 不参与运算

    ④String与任何基本数据类型使用连接符(+) 进行运算，都将自动串接成 String 类型

强制类型转换：大容量转小容量。需要使用强转符 "(需要转换的类型)"
                   但是可能损失精度。
## 六、运算符

算数运算符 :  +   -   +   -   *   /  %   前++  后++  前--  后--   +(连接符)

    //除法
    int a = 12;
    int b = 5;
    int c = a / b; //2
    
    //取模
    int c = 12 % 5;
    //前后++
    int i = 10;
    int j = i++;
    System.out.println(i);//11
    System.out.println(j);//10
    System.out.println(++i);
    int i = 10;
    i = i++; //10
    
    赋值运算符：  =   +=   -=   *=   /=   %=
    int i = 10;
    i += 5; //i = i + 5;
    System.out.println(i); //15

【面试题】

    short s = 5;
    
    s = s + 1;//编译？  NO
    
    s += 1; //编译？ YES      s = (short)(s + 1);
    
    比较运算符（关系运算符） :  ==    !=  >    <    >=   <=  （运算后结果都为 boolean 型）
    
    int a = 10;
    
    int b = 20;
    
    boolean b1 =  a == b;
    
    
    逻辑运算符： && -短路与   ||-短路或   !-逻辑非    &-逻辑与   |-逻辑或   ^-异或  （运算后结果都为 boolean 型）
    
    //需求：判断一个数是否大于10 小于20
    
    int a = 10;
    
    //10 < a < 20; 错误的做法
    boolean b2 = a > 10 && a < 20;

【面试题】 

    && 和  &  的区别？
    
    && ： 称为短路与，当左边表达式结果为 false 时，右边表达式将不再运算
    
    & ： 是位运算符，当用于逻辑运算时，无论左边表达式结果为true还是false，右边都运算
    
    位运算符 ：  ~    |   &  ^    <<  >>   >>>   注意：没有 <<<

三元运算符（三目运算符）

    条件表达式  ？  表达式1  :  表达式2;

    ①当条件表达式结果为 true 时，执行表达式1 ，否则执行表达式2

    ②表达式1和表达式2的结果类型需要保持一致！



## 七、流程控制：
顺序结构

分支结构
    条件判断：
            if(条件表达式){
                //当条件表达式结果为 true 时，需要执行的语句           
            }

            if(条件表达式){
                //当条件表达式结果为 true 时，需要执行的语句           
            }else{
                //当条件表达式结果为 false 时，需要执行的语句           
            }

            if(条件表达式1){
                //当条件表达式1 结果为 true 时，需要执行的语句           
            }else if(条件表达式2){
                //当条件表达式2 结果为 true 时，需要执行的语句           
            }else if(条件表达式3){
                //当条件表达式3 结果为 true 时，需要执行的语句
            }
            ……
            else{
                //当上述条件表达式结果都为 false 时，需要执行的语句           
            }
            注意：
                ①当某个条件表达式结果为true， 执行相应的语句，其他 else if 将不再执行
                ②if-else 语句可以嵌套的

选择结构：

           switch(表达式){
                case 值1 :
                    //执行的语句
                    break;
                case 值2 :
                    //执行的语句
                    //break;
                case 值3 :
                    //执行的语句
                    break;
                ……
                default :
                    //执行的语句
                    break;           
            }

            注意：
                ①表达式结果的数据类型，只能是 byte  short  char  int  枚举   String(jdk1.7后)
                ②表达式结果的数据类型要与case后值的类型需要保持一致！
                ③default 是可选的
                ④break 也是可选的，若与某个case后的值匹配成功，依次向下执行，直到遇到break为止。'
                ⑤case 后只能写常量值，不能写表达式

                //需求：若一个数大于2 小于5  打印 “2-5”
                int i = 2;
                switch(i){
                    case 1:
                        System.out.println("一");
                        break;
                    case 2:
                    case 3:   
                    case 4:                           
                    case 5:
                        System.out.println("2-5");
                        break;                                   
                }

循环结构：

①初始化值

②循环条件

③迭代条件

④循环体

    for(① ; ② ; ③){
        ④   
    }
    ①②④③②④③②④③②……④③②


    ①
    while(②){
        ④
        ③
    }

    ①
    do{
        ④
        ③
    }while(②);  
 
while 和 do-while 的区别？

while ： 先判断循环条件，再执行循环体

do-while : 先执行循环体，再判断循环条件。（至少执行一次） 
  
## 八、嵌套循环

一个循环充当了另一个循环的循环体

    打印100以内的质数：
    boolean flag = true;
    for(int i = 2; i <= 100; i++){
        for(int j = 2; j < i; j++){
            if(i % j == 0){
                flag = false;
                break;
            }
        }
        if(flag){
            System.out.println(i);   
        }
        flag = true;


## 九、特殊流程控制语句

break: 结束“当前”循环 。当用于switch-case语句时，用于结束当前 switch-case 语句

continue:  结束“当次”循环

    label:for(int i = 0; i < 100; i++){
        for(int j = 0; j < 100; j++){
            if(j == 13){
                System.out.println(j);
                break label;
            }
        }
    }