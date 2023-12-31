### C 语言数据类型归类

#### 整型类别

**char 字符型**：用 char 定义的变量是字符型变量，占 **1** 个字节，可以分别定义为：

- char 字符型：当直接声明一个 `char a`，这个 a 到底是有符号还是无符号是由编译器来决定的。可能是有符号的或者是无法符号的。

```c
// 用单引号引起单个字符正确，引起多个字符错误。
char ch1 = '1'; //正确
char ch2 = '1234' //错误
```

- unsigned char 无符号字符型：

```c
// 用单引号引起单个字符正确，引起多个字符错误。
unsigned char str = '1';  // 正确
unsigned char str = '123'; // 错误
```

- signed char 有符号字符型：

```c
// 用单引号引起单个字符正确，引起多个字符错误。
unsigned char str = '1';  // 正确
unsigned char str = '112'; // 错误
```

> 因为字符的本质就是 ASCII 码值，而 ASCII 码值 就是整型，所以被划分为整型类别。

**short 短整型**：用 short 定义的变量是短整型变量，占 **2** 个字节，可以分别定义为：

- short int 短整型：等价于 signed short [int] 有符号短整型。

```c
short int a = 10;
```

- unsigned short [int] 无符号短整型：

```c
unsigned short int a = 10;
```

- signed short [int] 有符号短整型：

```c
signed short int a = 10;
```

**int 整型**：用 int 定义的变量是整型变量，占 **4** 个字节，可以分别定义为：

- int 整型：等价于 signed int 有符号整型。

```c
int a = 10;
```

- unsigned int 无符号整型：

```c
unsigned int a = 10;
```

- signed int 有符号整型：`signed int xxx` 等价于 `int xxx`

```c
signed int a = 10;
```

**long 长整型**：用 long 定义的变量是长整型变量，占 **4（32 位）/8（64 位）** 个字节，可以分别定义为：

- long [int] 长整型：等价于 signed long [int] 有符号长整型。

```c
long int a = 10;
```

- unsigned long [int] 无符号长整型：

```c
unsigned long int a = 10;
```

- signed long [int] 有符号长整型：

```c
signed long int a = 10;
```

**long long 更长的整型**：用 long long 定义的变量是更长的整型变量，占 **8** 个字节，可以分别定义为：


- long long [int] 更长整型：等价于 signed long long [int] 有符号更长整型。

```c
long long int a = 10;
```

- unsigned long long [int] 无符号更长整型：

```c
unsigned long long int a = 10;
```

- signed long [int] 有符号更长整型：

```c
signed long long int a = 10;
```

> 提示：当需要定义的类型有正负值区分时，通常要用有符号的类型进行定义，当定义的类型不需要区分正负值或者不存在负数时，通常使用无符号的类型进行定义。

#### 浮点数类别

**float 单浮点数**：用 float 定义的变量是单浮点型变量，占 **4** 个字节：

```c
float a = 3.6f;
```

**double 双浮点型**：用 double 定义的变量是双浮点型变量，占 **8** 个字节：

```c
double a = 3.6;
```

> 浮点数类型通常用于表示小数，其中 float 类型的精度低，存储的数值范围较小，double 类型的精度高，存储的数值范围更大。

#### 构造类型

构造类型是由若干个相同或不同类型数据构成的集合，这种数据类型被称为构造类型。如：数组类型、结构体类型、联合类型、枚举类型。

**数组类型**：

#### 指针类型



### 数据存储

#### 大小端介绍

大小端模式之分的由来：

- 因为在计算机系统中，我们死以字节为单位的，每个地址单元都对应一个字节，一个字节为 8 bit，但是在 C 语言中，除了 8 bit 的 `char` 之外，还有 16 bit 的 `shot` 型，32 bit 的 `long` 型(具体需要看编译器)，另外，对于位数大于 8 位的处理器，例如 16 位或者 32 位的处理器，由于寄存器宽度大于一个字节，那么必然存在着一个如何将多个字节安排的问题。这就产生了大端存储模式和小端存储模式。

- 例如

大端**字节序**存储：把一个数据的高位字节序的内容存放在低地址处，把低位字节序的内容放在高地址处，就是大端字节序存储。

![image.png](http://43.143.27.249/image/d66e5798f56f6d10f8e63f263c9d8c78.png){{{width="100%" height="auto"}}}

小端**字节序**存储：把一个数据的高位字节序的内容存放在高地址处，把低位字节序的内容放在低地址粗，就是小端字节序存储。

![image.png](http://43.143.27.249/image/20bd0fee80a9951d8a1389eb6058d680.png){{{width="100%" height="auto"}}}

### 数组

#### 一维数组

#### 二维数组

### 操作符

操作符是用于执行各种操作和运算的富豪，在 C 语言中操作符可以分为这几种大类：**算术操作符**、**移位操作符**、**位操作符**、**赋值操作符**、**单目操作符**、**关系操作符**、**逻辑操作符**、**条件操作符**、**逗号表达式**、**下标引用、函数调用和结构成员操作符**。

#### 算术操作符

算术操作符有一下几种，分别是：

1. `+` 加法：用于进行数学加法运算。

2. `-` 减法：用于进行数学减法运算。

3. `*` 乘法：用于进行数学乘法运算。

4. `/` 除法：用于进行数学除法运算。需要注意的是，除法有**整型的除法**和**浮点数的除法**，其中整型的除法是，除数和被除数都是整型时，得数为整型。如果**除数和被除数至少有一个是浮点数时，得数就是浮点数**。

5. `%` 取模（求余）：用于进行数学取模（求余）运算。该操作符的两个操作数**必须为整数**，返回的是整除之后的余数。

#### 移位操作符

在使用移位操作符时，首先需要了解二进制数的表示和原码、补码、反码等相关的概念：

- **原码**：最高位为符号位（0 表示正数，1 表示负数），其余位表示数值的绝对值：

  - 正数 +6 的原码为：00000000000000000000000000000110。

  - 负数 -6 的原码为：10000000000000000000000000000110。

- **反码**：正数的反码与其原码相同，负数的反码是对**除符号位之外（符号位，也就是最高位不变）**的其它位逐位取反（0 变为 1，1 变为 0）所得到的值：

  - 正数 +6 的反码为：00000000000000000000000000000110。
  - 负数 -6 的反码为：11111111111111111111111111110001。

- **补码**：正数的补码与其原码相同，负数的补码是对其**反码末位加 1** 所得到的值。补码的一个重要性质是：减法运算可以转换为加法运算，即将减数的补码与被减数的补码相加，并且舍弃最高位的进位。即补码的加法运算可以直接应用于计算机的加法器，无需额外的处理。补码能够统一处理正数和负数，并且可以使用相同的运算规则进行加减运算。

  - 正数 +6 的补码为：00000000000000000000000000000110。
  - 负数 -6 的反码为：11111111111111111111111111110010。

> **总结**：正数的原码、反码和补码都相同，负数的原码是原码的符号位不变，其它位取反得到的值，负数的补码是对其反码末位加 1 所得到的值。在实际应用中，计算机系统通常使用补码来表示有符号整数，因为补码的运算规则更为简单。需要注意的是，对于一个由 n 位表示的补码，其最高位表示符号位，剩下的 n-1 位表示数值部分。

C 语言中的移位操作符用于对**二进制数的补码**进行位移操作，这是因为在内存中存的就是补码。移位操作符包括左移和右移两种形式，但需要要注意的是**移位操作符只适用于整数**：

1. `<<` 左移操作符：将某个数的所有位向左移动 n 个位置，右侧空出的位用 0 填充。

```c
#include <stdio.h>

int main() {
	int num = 6;
	int _num1 = num << 1;
	int _num2 = num << 2;
	int _num3 = num << 3;;
	int _num4 = num << 4;;
	printf("%d\n", num); // 6
	printf("%d\n", _num1); // 12 左移 1 位即可通过 6*2(6*2^1) 计算得出
	printf("%d\n", _num2); // 24 左移 2 位即可通过 6*4(6*2^2) 计算得出
	printf("%d\n", _num3); // 48 左移 3 位即可通过 6*8(6*2^3) 计算得出
	printf("%d\n", _num4); // 96 左移 4 位即可通过 6*16(6*2^4) 计算得出

	int num2 = -6;
	int num_1 = num2 << 1;
	int num_2 = num2 << 2;
	printf("%d\n", num_1); // -12 左移 1 位即可通过 -6*2(6*2^1) 计算得出
	printf("%d\n", num_2); // -24 左移 2 位即可通过 -6*4(6*2^2) 计算得出
}
```

2. `>>` 右移操作符：将某个数的所有位向右移动 n 个位置，左侧空出的位根据情况进行填充，可能用原符号位填充（带符号右移）或用 0 填充（无符号右移），一般来说是采用算术移位，即补充原符号位。

- 算术移位：右边丢失，左边补原符号位。

- 逻辑移位：右边丢失，左边补 0。

```c
signed int x = -10;  // 二进制表示为 1111 0110
signed int result = x >> 2;  // 右移2位，带符号右移，结果为 1111 1101，即十进制的-3
```

> **警告**：
> 1. 移位操作符只能针对整数进行操作，无法对浮点数进行操作。
> 2. 不要移动负数位，这个是标准未定义的。

#### 位操作符

C 语言中的位操作符是一组用于处理二进制位的运算符，包括按位与（&）、按位或（|）、按位异或（^）和按位取反（~）等操作，但需要要注意的是**位操作符只适用于整数**：

1. 按位与（&）：如果两个操作数的对应位（二进制位）上都为 1，则结果为 1，否则为 0。例如：

```c
unsigned int a = 60;    // 二进制表示为 0011 1100
unsigned int b = 13;    // 二进制表示为 0000 1101
unsigned int result = a & b;  // 结果为 0000 1100 (12)
```

> 两个数的二进制对应位都 1，则为 1，否则为 0。

2. 按位或（|）：如果两个操作数中有一个对应位（二进制位）上为 1，则结果为 1，否则为 0。例如：

```c
unsigned int a = 60;  // 二进制表示为 0011 1100
unsigned int b = 13;  // 二进制表示为 0000 1101
unsigned int result = a | b;  // 结果为 0011 1101 (61)
```

> 两个数的二进制对应位只要有 1，则为 1，否则为 0。

3. 按位异或（^）：如果两个操作数对应位（二进制位）上不相同，则结果为 1，否则为 0。例如：

```c
unsigned int a = 60;  // 二进制表示为 0011 1100
unsigned int b = 13;  // 二进制表示为 0000 1101
unsigned int result = a ^ b;  // 结果为 0011 0001 (49)
```

> 两个数的二进制对应位不相同为 1，相同则为 0。

> **说明**：
> 
> - **两个相同的数按位异或为 0**。
> 
> - **0 和任何一个整数按位异或为该整数**。
> 
> ```c
> #include <stdio.h>
> 
> int main() {
> 	int a = 12;
>   int b = 12;
>   int c = a ^ b;
>   printf("%d\n", c); // 0
>   
>   int _a = 0;
>   int _b = 12;
>   int _c = _a ^ _b;
>   printf("%d\n", _c); // 12
> 
> 	return 0;
> }
> ```

4. 按位取反（~）：对操作数的每个位（二进制位）取反，即 0 变为 1，1 变为 0。例如：

```c
unsigned int a = 60;  // 二进制表示为 0011 1100
unsigned int result = ~a;  // 结果为 1100 0011（-61）(补码形式，实际结果需依据具体数据类型进行解释)
```

> 一个数的二进制位是 1 时，为 0，是 0 时，则为 1。

#### 移位操作符与位操作符的使用示例

实现一个整数存储在内存中的二进制 1 的个数:

```c
#include <stdio.h>

int countSetBits(int n) {
	int count = 0;
	while (n) {
		count += n & 1;
		n >>= 1;
	}
	return count;
}

int main() {
	int num = 1209;
	int count = countSetBits(num);
	printf("整数 %d 存储在内存中的二进制表示中包含 %d 个 1\n", num, count);
	return 0;
}
```

#### 赋值操作符

C 语言中的赋值操作符用于将一个值赋给变量，也就是将右边的表达式的结果赋给左边的变量。在 C 语言中，赋值操作符有多种类型，包括：

1. 简单赋值（=）：将右侧表达式的值赋给左侧变量：

```c
#include <stdio.h>

int main() {
  int a = 0;
	printf("赋值前 a=%d\n", a); // 0
  a = 12;  // 将整数 12 赋给整型变量 a
	printf("赋值后 a=%d\n", a); // 12
	return 0;
}
```

2. 加等于（+=）：将右侧表达式的值加到左侧变量上：

```c
#include <stdio.h>

int main() {
  int a = 9;
	printf("赋值前 a=%d\n", a); // 9
  a += 3;
	printf("赋值后 a=%d\n", a); // 12
	return 0;
}
```

3. 减等于（-=）：将右侧表达式的值从左侧变量中减去：

```c
#include <stdio.h>

int main() {
  int a = 12;
	printf("赋值前 a=%d\n", a); // 12
  a -= 3;
	printf("赋值后 a=%d\n", a); // 9
	return 0;
}
```

4. 乘等于（*=）：将右侧表达式的值乘以左侧变量的值：

```c
#include <stdio.h>

int main() {
  int a = 2;
	printf("赋值前 a=%d\n", a); // 2
  a *= 6;
	printf("赋值后 a=%d\n", a); // 12
	return 0;
}
```

5. 除等于（/=）：将左侧变量的值除以右侧表达式的值：

```c
#include <stdio.h>

int main() {
  int a = 12;
  printf("赋值前 a=%d\n", a); // 12
  a /= 2;
  printf("赋值后 a=%d\n", a); // 6
  return 0;
}
```

6. 取模等于（%=）：将左侧变量的值模以右侧表达式的值：

```c
#include <stdio.h>

int main() {
  int a = 12;
  printf("赋值前 a=%d\n", a); // 12
  a %= 9;
  printf("赋值后 a=%d\n", a); // 3
  return 0;
}
```

7. 左移等于（<<=）：将左侧变量的值左移若干位（由右侧表达式指定）：

```c
#include <stdio.h>

int main() {
  int a = 6;
  printf("赋值前 a=%d\n", a); // 6
  a <<= 1;
  printf("赋值后 a=%d\n", a); // 12
  return 0;
}
```

8. 右移等于（>>=）：将左侧变量的值右移若干位（由右侧表达式指定）：

```c
#include <stdio.h>

int main() {
  int a = 12;
  printf("赋值前 a=%d\n", a); // 12
  a >>= 1;
  printf("赋值后 a=%d\n", a); // 6
  return 0;
}
```

9. 位与等于（&=）：将左侧变量的值与右侧表达式的值进行位与运算：

```c
#include <stdio.h>

int main() {
  int a = 12;
  printf("赋值前 a=%d\n", a); // 12
  a &= 9; // 相当于 a = a & 9;
  printf("赋值后 a=%d\n", a); // 8
  return 0;
}
```

10. 位或等于（|=）：将左侧变量的值与右侧表达式的值进行位或运算：

```c
#include <stdio.h>

int main() {
  int a = 12;
  printf("赋值前 a=%d\n", a); // 12
  a |= 9; // 相当于 a = a | 9;
  printf("赋值后 a=%d\n", a); // 13
  return 0;
}
```

11. 位异或等于（^=）：将左侧变量的值与右侧表达式的值进行位异或运算：

```c
#include <stdio.h>

int main() {
  int a = 12;
  printf("赋值前 a=%d\n", a); // 12
  a ^= 9; // 相当于 a = a ^ 9;
  printf("赋值后 a=%d\n", a); // 5
  return 0;
}
```

> 在使用赋值操作符时，右侧的表达式会在赋值之前被求值。因此，如果右侧的表达式中包含其他变量或函数调用，那么这些变量或函数会在赋值之前被求值。

#### 单目运算符

单目运算符表示操作数只有一个，具体有以下一些类型：

1. 逻辑非（!）运算符：用于对表达式求逻辑非，结果为真（非零）或假（零）：

- 非零值求逻辑非（!）结果为 0（假）：

```c
#include <stdio.h>

int main() {
	int a = 9;
	printf("%d\n", !a);  // 输出 0，因为 a 的值非零，取逻辑非结果为假
	return 0;
}
```

- 零值求逻辑非（!）结果为 1（真）：

```c
#include <stdio.h>

int main() {
	int a = 0;
	printf("%d\n", !a);  // 输出 1，因为 a 的值为零，取逻辑非结果为真
	return 0;
}
```

2. 递增（`++`）运算符：用于增加变量的值：

- 前缀递增（++var）：在表达式被求值之前，先对变量进行自增或自减操作，然后返回新值：

```c
#include <stdio.h>

int main() {
	int a = 8;
	int b = ++a;  // a 自增为 9，b 的值为 9
	printf("赋值后 b=%d\n", b); // b=9
	return 0;
}
```

> `++a` 表示先自增再执行。

- 后缀递增（var++）：在表达式被求值之后，对变量进行自增操作，返回旧值：

```c
#include <stdio.h>

int main() {
	int a = 8;
	int b = a++;  // a 自增为 9，b 的值为 9
	printf("赋值后 b=%d\n", b); // b=8
	return 0;
}
```

> `a++` 表示限执行后自增。

3. 递减（`--`）运算符：用于减少变量的值：

- 前缀递增（--var）：在表达式被求值之前，先对变量进行自增或自减操作，然后返回新值：

```c
#include <stdio.h>

int main() {
	int a = 9;
	int b = --a;  // a 自减为 8，b 的值为 8
	printf("赋值后 b=%d\n", b); // b=8
	return 0;
}
```

> `--a` 表示先自减再执行。

- 后缀递增（var--）：在表达式被求值之后，对变量进行自增操作，返回旧值：

```c
#include <stdio.h>

int main() {
	int a = 9;
	int b = a--;  // a 自增为 8，b 的值为 9
	printf("赋值后 b=%d\n", b); // b=9
	return 0;
}
```

> `a--` 表示限执行后自减。

4. 取地址（&）运算符：用于获取变量的内存地址：

```c
#include <stdio.h>

int main() {
	int a = 12;
	int *ptr = &a;  // 将变量 a 的地址赋给指针 ptr
	printf("赋值后 ptr=%p\n", ptr); // ptr=00CFF7E0
	return 0;
}
```

5. 解引用（*）运算符：用于访问指针所指向的内存地址中的值：

```c
#include <stdio.h>

int main() {
  int a = 12;
  int *ptr = &a;
  printf("%d\n", *ptr);   // 输出 12，访问指针 ptr 所指向的值
	return 0;
}
```

6. 正号（+）和负号（-）运算符：用于表示正数和负数：

- 正号（+）：不改变操作数的值，保持为正数：

```c
#include <stdio.h>

int main() {
  int a = +5;   // a 的值为 5
  printf("%d\n", a);   // 5
	return 0;
}
```

- 负号（-）：求操作数的相反数：

```c
#include <stdio.h>

int main() {
  int a = -5;   // a 的值为 -5
  printf("%d\n", a);   // -5
	return 0;
}
```

7. 按位取反（~）运算符：对操作数的每个位进行取反操作：

- 对于整数，按位取反操作将每个二进制位取反（0 变为 1，1 变为 0）：

```c
#include <stdio.h>

int main() {
  int a = 5;   // 二进制为 0000 0101
  printf("%d\n", ~a);   // 输出 -6，按位取反后得到 1111 1010（补码形式）
	return 0;
}
```

- 对于字符类型，按位取反操作将字符编码的每个位取反：

```c
#include <stdio.h>

int main() {
  char ch = 'A';   // ASCII 编码为 65，二进制为 0100 0001
  printf("%d\n", ~ch);   // 输出 -66，按位取反后得到 1011 1110（补码形式）
	return 0;
}
```

8. sizeof 操作符：操作数的类型长度（以字节为单位），也可以说计算的是变量所占内存空间的大小：

```c
#include <stdio.h>

int main() {
	int a = 12;

	// 计算的是 a 所占内存的大小，单位是字节
	int n = sizeof(a);
	printf("%d\n", n); // 4

	// 计算类型所创建的变量占据空间的大小
	int _n = sizeof(int);
	printf("%d\n", _n); // 4

	// 计算数组所占内存空间的大小
	int arr[5] = { 0 };
	printf("%d\n", sizeof(arr)); // 20

	return 0;
}
```

sizeof 面试题：

```c
#include <stdio.h>

void test1(int arr[]) {
	// arr 是指针，所以长度是 4
	printf("%d\n", sizeof(arr)); // 4
}

void test2(char ch[]) {
	// ch 也是指针，所以长度是 4
	printf("%d\n", sizeof(ch)); // 4
}

int main() {
	int arr[10] = { 0 };
	char ch[10] = { 0 };   // 将整型变量 a 转换为浮点型变量 b
	// 计算整个数组所占内存空间的大小，所以是 40
	printf("%d\n", sizeof(arr)); // 40
	// ch 是字符类型，长度是 10
	printf("%d\n", sizeof(ch)); // 10

	test1(arr);
	test2(ch);

	return 0;
}
```

9. 类型转换运算符：用于将一个数据类型转换为另一个数据类型：

```c
#include <stdio.h>

int main() {
  int a = 9;
  float b = (float)a;   // 将整型变量 a 转换为浮点型变量 b

  printf("%.2f\n", b); // 保留两位小数 9.00

  return 0;
}
```

#### 关系操作符

在 C 语言中，关系操作符用于比较两个值之间的关系，并返回一个布尔值（0或1），对于关系操作符具体有以下一些类型：

1. 大于关系（>）：用于检查左操作数是否大于右操作数。如果是，则返回 1，否则返回 0。

2. 小于关系（<）：用于检查左操作数是否小于右操作数。如果是，则返回 1，否则返回 0。

3. 相等关系（==）：用于检查两个操作数是否相等。如果相等，则返回 1，否则返回 0。

4. 不等关系（!=）：用于检查两个操作数是否不相等。如果不相等，则返回 1，否则返回 0。

5. 大于等于关系（>=）：用于检查左操作数是否大于或等于右操作数。如果是，则返回 1，否则返回 0。

6. 小于等于关系（<=）：用于检查左操作数是否小于或等于右操作数。如果是则返回 1，否则返回 0。

> 注意：如果需要比较两个字符串是否相等，不能使用 `==` 进行比较，因为使用 `==` 比较两个字符串时（`"abc" == "abcd"`），实际是在比较两个字符串的地址。正确的做法是通过库函数 `strcmp` 进行比较。

#### 逻辑操作符

C 语言中的逻辑操作符用于对表达式进行布尔运算，判断条件的真假以及控制程序的流程，具体有以下几种类型：

1. 逻辑与（&&）：表示当且仅当两个操作数都为真时，结果为真，否则结果为假。

```c
int a = 12
int b = 9;
if (a > 0 && b > 0) {
  // 当 a 和 b 都大于 0 时执行
}
```

2. 逻辑或（||）：表示当两个操作数中至少一个为真时，结果为真，如果两个操作数都为假，结果为假。

```c
int a = 12
int b = -9;
if (a > 0 || b > 0) {
  // 当 a 或 b 中有一个大于 0 时执行
}
```

> 逻辑与（&&）与逻辑或（||）只关注真假，不关心二进制的位数。

逻辑与（&&）与逻辑或（||）相关笔试题：

```c
#include <stdio.h>

void test1() {
	int i = 0, a = 0, b = 2, c = 3, d = 4;

	i = a++ || ++b || d++;

  // a = 1 b = 3 c = 3 d = 4
	printf("a = %d b = %d c = %d d = %d\n", a, b, c, d);
}

void test2() {
	int i = 0, a = 1, b = 2, c = 3, d = 4;

	i = a++ || ++b || d++;

  // a = 2 b = 2 c = 3 d = 4
	printf("a = %d b = %d c = %d d = %d\n", a, b, c, d);
}


void test3() {
	int i = 0, a = 0, b = 2, c = 3, d = 4;

	i = a++ && ++b && d++;

  // a = 1 b = 2 c = 3 d = 4
	printf("a = %d b = %d c = %d d = %d\n", a, b, c, d);
}

void test4() {
	int i = 0, a = 1, b = 2, c = 3, d = 4;

	i = a++ && ++b && d++;

  // a = 2 b = 3 c = 3 d = 5
	printf("a = %d b = %d c = %d d = %d\n", a, b, c, d);
}

int main() { 
	test1();
	test2();
	test3();
	test4();

	return 0;
}
```

> **说明**：
>
> - && 操作符左边为假，则 && 的右边不再进行计算。
>
> - || 操作符左边为真，则 || 的右边不再进行计算。

#### 条件操作符（三目操作符）

C 语言中的条件操作符是一种特殊的运算符，用于根据条件选择表达式的值，语法为：

```c
expression1 ? expression2 : expression3
```

> expression1 是一个条件表达式，如果它的值为真（非零），则整个表达式的值为 expression2 的值；否则，整个表达式的值为 expression3 的值，即：
>
> - 如果 expression1 的值为真，则 expression2 计算，expression3 不进行计算。expression2 的结果就是整个表达式的结果。
>
> - 如果 expression1 的值为假，则 expression2 不计算，expression3 进行计算。expression3 的结果就是整个表达式的结果。

具体使用方式为：

```c
#include <stdio.h>

int max(int a, int b) {
  return (a > b) ? a : b;  // 如果 a 大于 b，则返回 a；否则返回 b
}

int main() {
  int a = 12;
  int b = 9;

	int num = max(a, b);
  printf("%d\n", num); // 12

	return 0;
}
```

#### 逗号（,）表达式

C 语言中的逗号表达式是一种特殊的运算符，用于在一个表达式中多次使用逗号分隔多个子表达式，并按顺序（从左到右）依次计算这些子表达式。**整个表达式的结果是最后一个表达式的结果**。语法形式为：

```c
expression1, expression2, expression3, ..., expressionn
```

> 逗号表达式的计算过程为：从左到右依次计算每个子表达式，并**返回最后一个子表达式的值**作为整个逗号表达式的值。

具体使用示例如下：

- 示例一：

```c
#include <stdio.h>

int test1() {
	int a = 1;
	int b = 2;
	int c = (a > b, a = b + 10, a, b = a + 1); // 12 => 13 
	printf("%d\n", c); // 13
}

int test2() {
	int a = 0;
	int b = 1;
	int c = 2;
	int d = c;
	if (a = b + 1, c = a / 2, d > 0) {
		printf("%d\n", d); // 2
	}
}

int main() {
	test1();
	test2();

	return 0;
}
```

- 示例二，使用逗号表达式优化 while 循环中冗余的代码：

```c
int a = 0;

a = get_val();
count_val(a);

while(a > 0) {
  a = get_val();
  count_val(a);
  // ...
}

// 使用逗号表达式改写上述代码：
while(a = get_val(), count_val(a), a > 0) {
  // ...
}
```

#### 下标引用、函数调用和结构成员

1. `[]` 下标引用操作符：用于操作数组，操作数是：一个数组名 + 一个索引值：

```c
#include <stdio.h>

int main() {
  int arr[10]; // 创建数组
  arr[9] = 12; // 使用下标引用操作符
  6[arr] = 9;
  printf("%d\n", arr[9]); // 12
  printf("%d\n", arr[6]); // 9

  return 0;
}
```

> **说明**：
>
> - arr 是数组首元素的地址。
>
> - `arr + 9` 表示跳过 9 个元素，指向第 10 个元素。`*(arr + 9)` 表示的就是第 10 个元素。因此可以认为：`arr[9]` 等价于 `*(arr + 9)` 等价于 `*(9 + arr)` 也就等价于 `9[arr]`。
>
> - 但是不建议将 `arr[9]` 写成 `9[arr]`。

2. 函数调用：函数调用用于执行函数中的代码块，并可以传递参数和获取返回值：

```c
int add(int a, int b) {
  return a + b;
}

int result = add(9, 12);  // 调用 add 函数，result 的值为 21
```

> 上述代码 `add()` 上的 `()` 就是函数调用操作符，操作数是：`add、a、b`。

3. 结构成员：结构成员用于访问结构体中的具体成员变量：

- 直接在函数内部定义结构体并给结构体赋值：

```c
#include <stdio.h>
#include  <string.h>

int main() {
	struct Person {
		char name[20];
		int age;
	};

	struct Person person1 = { 0 };
  /* 
    person1.name = "dnhyxc"; 该写法是错误的，
    因为 .name 指向的是一个地址，因此无法将 "dnhyxc" 复制给一个地址。
    因此需要使用 strcpy 进行赋值。
  */
	strcpy(person1.name, "dnhyxc");
	person1.age = 18;

	printf("Name: %s, Age: %d\n", person1.name, person1.age);  // 输出 Name: dnhyxc, Age: 18
	return 0;
}
```

- 结构体和赋值不在同一个函数中时，需要通过传递地址进行结构体赋值：

```c
#define _CRT_SECURE_NO_WARNINGS  // 解决编译报错问题

#include <stdio.h>
#include <string.h>

struct Person {
	char name[20];
	int age;
};

// 写法一
void createPer1(struct Person* ps) {
	strcpy((*ps).name, "dnhyxc");
	(*ps).age = 18;
}

// 写法二
void createPer2(struct Person* ps) {
	strcpy(ps->name, "dnhyxc");
	ps->age = 18;
}

// 写法一
void printPer1(struct Person ps) {
	printf("Name: %s, Age: %d\n", ps.name, ps.age);  // 输出 Name: dnhyxc, Age: 18
}

// 写法二
void printPer2(struct Person* ps) {
	printf("Name: %s, Age: %d\n", ps->name, ps->age);  // 输出 Name: dnhyxc, Age: 18
}

int main() {
	struct Person person1 = { 0 };

	createPer1(&person1);
	createPer2(&person1);

	printPer1(person1);
	printPer2(&person1);

	return 0;
}
```

> 上述 `createPer1` 中的写法等价于 `createPer2` 中的写法，`printPer1` 中的写法等价于 `printPer2` 中的写法，但是需要注意 `printPer1` 及 `printPer2` 的传参，`printPer2` 需要传递地址。

### static 关键字

static 是用来修饰变量和函数的：

- 修饰局部变量：称为静态局部变量。

- 修饰全局变量：称为静态全局变量。

- 修饰函数：称为静态函数。

#### 修饰局部变量

在一般情况下，局部作用域的变量生命周期是进入作用域时创建，出作用域时销毁。因此局部作用域中的变量就在每次执行时创建，执行完毕之后销毁。
而通过 static 修饰过后，局部变量出了作用域，该局部变量也不会被销毁。

static 修饰局部变量的本质就是 static 改变了变量的存储位置。原本局部变量时存放在栈区中的，但被 static 修饰过后，就会把变量存放到「静态区」。也就相当于延长了变量的生命周期，将该变量的生命周期变成了与程序的生命周期一样，只有当程序运行结束后，该变量才会被销毁。

```c
#include "stdio.h"

void test() {
  // 局部作用域的变量生命周期是进入作用域时创建，出作用域时销毁，即每次进入时，a 都会重新创建并赋值为1。
  int a = 1;
  a++;
  printf("%d ", a); // 2 2 2 2 2 2 2 2 2 2
}

void test_static () {
  // static 声明的局部变量不会被重新创建，会保存上一次执行完毕的值。
  static int a = 1;
  a++;
  printf("%d ", a); // 2 3 4 5 6 7 8 9 10 11
}

int main() {
  int i = 0;
  while (i < 10) {
    test();
    test_static();
    i++;
  }
  return 0;
}
```

#### 声明全局变量

正常情况下，全局变量都是具有外部链接属性的，也就是说，其他的源文件（.c 后缀的文件）如果想使用某个变量时，可以使用「extern」关键字引入即可。但如果使用 static 修饰全局变量的时候，这个全局变量的外部链接属性就会变成内部链接属性，而这就会使得其它源文件不能再通过「extern」关键字使用这个全局变量，只能在声明该变量的源文件中使用了。

在 add.c 文件中创建如下全局变量：

```c
// 在 add.c 文件中创建如下全局变量

int g_val = 120902;

static int g_val2 = 1209021101;
```

在 test.c 文件中使用 add.c 中声明的变量

```c
#include "stdio.h"

extern int g_val; // 引入 add.c 中声明的全局变量
extern int g_val2; // 引入 add.c 中使用static声明的全局变量

int main() {
  printf("%d\n", g_val); // 120902
  printf("%d\n", g_val2); // 运行会报错，因为该全局变量使用static修饰了
  return 0;
}
```

#### 声明函数

函数原本是具有外部链接属性的，但是当一个函数被 static 修饰过后，该函数的外部链接属性就会变成内部链接属性，从而使得其它源文件无法通过「extern」使用该函数。

在 add.c 文件中创建如下函数：

```c
int Add (int x, int y) {
  return x + y;
}
```

在 test.c 文件中调用 add.c 中声明的函数：

```c
#include "stdio.h"

extern int Add(int x, int y); // 引入 add.c 中声明的函数

int main() {
  int sum = Add(12, 9);
  printf("%d", sum); // 21
  return 0;
}
```

### #difine

`#define` 用于定义预处理器宏。预处理器宏是一种文本替换机制，它告诉编译器在编译代码之前将指定的文本替换为特定的值或表达式。

基本的语法格式如下：

```c
#define 宏名 宏体
```

> 说明：**宏名**是你自定义的标识符，**宏体**可以是常量、变量、表达式等。

#### #difine 定义标识符常量

```c
#include <stdio.h>

// 定义标识符常量
#define MAX 999

int main () {
  printf("%d\n", MAX);

  int n = MAX;
  printf("%d\n", n);

  // MAX 是一个常量，因此可以作为数组的长度限制
  int arr[MAX] = { 0, 1, 2 }
  printf("%d\n", arr);

  return 0;
}
```

#### #define 定义宏

```c
#include <stdio.h>

// 定义宏
#define ADD(x, y) ((x) + (y));

int main () {
  int a = 12;
  int b = 9;
  int sum = ADD(a, b)
  
  printf("%d\n", sum);

  return 0;
}
```

### 指针学习前提

指针与计算机内存息息相关，因此想要充分的了解指针，就需要先了解内存是什么。而要想清晰的认识内存，那就需要弄懂 **bit(位)** 和 **byte(字节)**。

[参考资料](https://zhuanlan.zhihu.com/p/101934152)

[参考资料](https://zhuanlan.zhihu.com/p/41187907)

#### bit（位） 和 byte（字节）

bit（位）是计算机系统中最小的**存储单位**，众所周知计算机实质是通过二进制数 0 或 1 来存储数据的，因此可以看成存放 1 个二进制数字的 1 个位置。也就是说，bit 只有两种值，0 或者 1。也就是 2^1 = 2 种不同的状态。

byte（字节）是计算机系统中最小的可寻址**内存单元**。8 个 bit 位被组合成一个字节（byte），也就是说 8 bit 可以存储一个字节的数据。因为 1 bit 有 2^1（2）种状态，所以一个字节可以表示 2^8（2 × 2 × 2 × 2 × 2 × 2 × 2 × 2）= 256 种不同的状态，即从 0 到 255。

![image.png](http://43.143.27.249/image/6e8ed63d48797bc7415522054bea6a9d.png){{{width="100%" height="auto"}}}

一个字节（1 byte）可以存储整数、字符、布尔值等各种类型的数据。例如：

- 数值 255 需要 8 个位来存放，即一个字节。这是因为 8 位可以表示 0 - 255 的数值，即（2^8）种状态，所以需要 8 位来表示 255。

- 数值 100 需要用 7 位来存放，因为 7 位就可以表示 0 - 128 的数值，也就是（2^7）种状态，因此 100 只需要 7 位即可表示出来了。

#### 内存

内存是电脑上特别重要的存储器，计算机中程序的运行都是在内存中进行的。因此为了有效的使用内存，就把内存划分成了一个个小的内存单元，每个内存单元的大小是**1 个字节(1byte)**。

为了能够有效的访问到内存的每个单元，就给内存单元进行了编号，这些编号被称为该内存单元的**地址**。如下图所示：

![image.png](http://43.143.27.249/image/7c7aa3038bd2ca32f2a0e7c685bbc757.png){{{width="100%" height="auto"}}}

对于 32 位的系统，由于有 32 位的地址空间，每个地址可以用 32 个二进制位来表示。而每个二进制位上可以有两种状态（0 或 1），因此可以用 2^32 来表示不同的地址组合。这意味着 32 位操作系统最多可以支持 2^32 个地址，也就是 4,294,967,296 个不同的内存单元（4,294,967,296B）。

说到这，那么问题就来了，4,294,967,296B 是如何算出来是 4GB 的容量呢？对此，我们可以对其进行换算一下：

因为 1KB 等于 1024B，所以 4,294,967,296B 就等于 4,194,304KB，而 1MB 等于 1024 KB，所以 4,194,304KB 就等于 4096MB，由于 1G 等于 1024MB，所以 4096MB 就等于 4G，因此 4,294,967,296B 就相当于 4G 的内存容量。即 `4,294,967,296B = 4,194,304KB = 4096MB = 4G`。

### 指针

在 C 语言中，指针是一种特殊的变量类型，它存储了一个变量的内存地址。指针可以用来访问和修改该内存地址中存储的数据。

使用指针需要先定义指针变量，然后将其初始化为一个实际变量的地址（或者使用动态内存分配函数分配一块内存，然后将指针指向该内存块的地址）。例如：

```c
int x = 12;

int *p; // 定义一个指向整型变量的指针 p

p = &x; // 将指针 p 指向变量 x 的地址

char s = 'n';

char *ps; // 定义一个指向字符型的指针 ps

ps = &s; // 将指针 ps 指向变量 s 的地址
```

上述 `*` 符号表示 `p` 和 `ps` 是一个指针变量，用于存放变量的地址。 `int *p` 表示指向整型数据的指针地址，`char *ps` 表示指向字符型数据的指针地址。

**总结**：指针就是地址，口语中说的指针通常指的是指针变量。

#### 指针变量的大小

对于 32 位的操作系统，地址是由 32 个 bit 位表示的，即 4 个字节。

对于 64 位的操作系统，地址是由 64 个 bit 位表示的，即 8 个字节。

至于为什么能得出上述的结论，容我慢慢道来：

在 32 位系统中，CPU 的寻址空间大小是 32 位，也就是说可以寻址的内存空间大小为 2^32 个字节（即 4GB）。为了能够**唯一地标识**每个内存地址，需要使用一个长度为 **32bit** 的二进制数字来表示，也就是 **4byte**。而对于 64 位的系统，就需要长度为 **64bit** 的二进制数来表示内存地址，即 **8byte**，从而确保内存地址的唯一性。

```c
#include "stdio.h"

int main() {
  printf("%zu\n", sizeof(int*)) // 32 位为 4，64 位为8
  printf("%zu\n", sizeof(char*)) // 32 位为 4，64 位为8
  printf("%zu\n", sizeof(short*)) // 32 位为 4，64 位为8
  printf("%zu\n", sizeof(double*)) // 32 位为 4，64 位为8

  return 0;
}
```

#### 指针类型的意义

指针类型决定了指针在解引用的时候访问几个字节，如果是 `int*` 指针，解引用时访问**4个字节**，如果是 `char*` 的指针，解引用时访问**1个字节**，而对于 `double*` 的指针类型，解引用时访问**8个字节**。

指针类型同时还决定了指针 `+（加）、-（减）`操作的时候跳过几个字节（指针的步长），如下：

```c
#include "stdio.h"

int main() {
  int a = 0x11223344;
	int* pa = (char*)&a;
	char* pc = (char*)&a;

	// 从 pa（006FF9F8）到 pa + 1（006FF9FC）总共跳过了 4 个字节
	printf("pa = %p\n", pa); // 006FF9F8
	printf("pa+1 = %p\n", pa+1); // 006FF9FC

	// 从 pc（006FF9F8）到 pc + 1（006FF9F9）总共跳过了 1 个字节
	printf("pc = %p\n", pc); // 006FF9F8
	printf("pc+1 = %p\n", pc+1); // 006FF9F9

  return 0;
}
```

> 由上述说明可以得出：指针类型不能随便定义，需要针对每个特定的类型定义对应的指针类型，防止出现不必要的错误。

### 野指针

野指针表示的就是指针指向的位置是不可知的，即是随机的，不正确的，没有明确限制的。

#### 造成野指针的原因

1. **指针未初始化**：在定义指针式，如果没有对其进行初始化，那么指针变量将会存储一个未知的值，这个值可能是 0，也有可能是一个随机的地址。如果在使用这样的指针变量时，就有可能访问到野指针，从而导致程序崩溃，如：

```c
char* p; // p 未初始化

*p = 9; // 这里的 p 就是野指针

printf("%s", p); // 这里打印的 p 也是野指针
```

2. **指针越界访问**：当使用指针访问数组时，如果指针超出了数组的边界，就有可能访问到野指针。这是因为指针变量的值实际上是一个地址，如果这个地址不再数组范围内，那么就会访问到非法指针，如：

```c
int arr[10] = {1, 2, 3, 4, 5};

int* p = &arr[0];

printf("%d", *(p + 11)); // 这里已经越界访问了，导致了野指针
```

3. **指针指向的空间释放**：在指针释放后，没有将指针置为 `NULL` 或者重新指向有效的内存地址。当程序试图使用野指针时，由于指针指向的内存已经释放，操作系统会将该内存重新分配给其他变量或释放掉，因此野指针的解引用操作将访问无效的内存区域。

```c
#include <stdio.h>

int* test() {
	int a = 10;

	return &a;
}

int main() {
	/* 
		由于 test 方法调用完成之后，变量 a 就会销毁，而 p 还记录了已经销毁的 a 的地址，
		这就会导致出现野指针。因为在 a 销毁之后，指针 p 保存的指针地址就不再是指向原来的 a 了。
	*/
	int* p = test();

	return 0;
}
```

#### 如何避免出现野指针

1. 在释放指针所指向的内存后，将指针设置为 NULL，以避免继续使用已释放的内存地址。

2. 避免对未初始化的指针进行解引用操作。

3. 注意指针的作用域和生命周期，确保指针指向的内存空间在使用期间是有效的。

4. 在重新分配内存时，确保先释放旧的内存再分配新的内存，并将指针指向新的内存地址。

5. 对数组进行循环或者通过下标取值时，确保没有越界。

### 指针运算

#### 指针 + - 整数

使用指针与整数进行加减运算，这种运算通常用于指针的偏移操作，可以使指针指向数组中的不同元素或者在内存中移动到其他位置。

具体来说，当一个指针与一个整数相加时，意味着将指针向后移动了若干个元素，每个元素占据的字节取决于指针所指向的类型。例如，对于一个指向int类型的指针，每移动一个单位就会跨过一个int大小的字节。

当一个指针与一个整数相减时，意味着将指针向前移动了若干个元素，如：

- 示例一：

```c
int arr[5] = {1, 2, 3, 4, 5};
int *p = arr;  // 指向数组第一个元素

p = p + 2;  // 将指针向后移动两个元素，p 指向数组的第三个元素
printf("%d\n", *p);  // 输出 3

p = p - 1;  // 将指针向前移动一个元素，p 指向数组的第二个元素
printf("%d\n", *p);  // 输出 2
```

- 示例二：

```c
#include <stdio.h>

int main() {
  int arr[10] = { 0 };

  int i = 0;

  int sz = sizeof(arr) / sizeof(arr[0]);

  int* p = arr;

	// 方式一
	// for(i = 0; i < sz; i++) {
  //   *p++ = 1;
  // }

	// 方式二，等价于方式一
  for(i = 0; i < sz; i++) {
    *(p + i) = 1; // 将数组 arr 全部赋值为 1
  }

  int j = 0;

  for(j = 0; j < sz; j++) {
    printf("%d ", arr[j]); // 1 1 1 1 1 1 1 1 1 1 
  }

  return 0;
}
```

#### 指针 -（减）指针

不是所有的指针都能够相减，只有指向同一快空间的两个指针才能相减，如：

```c
#include <stdio.h>

int main() {
	int arr[10] = { 0 };

	int str[10] = { 0 };

	printf("%d\n", &arr[10] - &str[9]); // 该写法是没有意义的

	return 0;
}
```

> 上述两个指针相减的写法就是错误的，因为这没有意义，因此需要避免这种写法。

一个指针减去另一个指针的绝对值，得到的就是两个指针之间的**元素个数**，如：

```c
#include <stdio.h>

int main() {
	int arr[10] = { 0 };

	printf("%d\n", &arr[9] - &arr[0]); // 9
	printf("%d\n", &arr[0] - &arr[9]); // -9

	return 0;
}
```

> 上述代码 `&arr[9]` 和 `&arr[0]` 分别表示 arr 下标为 9 的元素和下标为 0 的元素的指针。

指针减去指针的实际使用：

- 计算字符长度：

```c
#include <stdio.h>

long myStrlen(char* str) {
  char* start = str;

  while(*str != '\0') {
    str++;
  }

  // 当循环结束时，str 就是字符的最后一个地址，通过最有一个地址减去第一个地址，所得的就是字符长度
  return (str - start);
}

int main() {
  char str[6] = "dnhyxc";

  long num = myStrlen(str);

  printf("%ld\n", num);

  return 0;
}
```

#### 指针的关系运算

指针可以进行关系运算（比较运算符），用于比较两个指针之间的关系。下面是几种常见的指针关系运算：

1. **相等性比较**：使用 == 运算符来比较两个指针是否相等。如果两个指针指向相同的内存地址，则它们被认为是相等的；否则，它们被认为是不相等的。

```c
int *p1 = /* 指向某个内存地址 */;
int *p2 = /* 指向另一个内存地址 */;

if (p1 == p2) {
  // 指针 p1 和 p2 相等
} else {
  // 指针 p1 和 p2 不相等
}
```

2. **关系比较**：使用 <、>、<=、>= 运算符来比较两个指针所指向的内存地址的大小关系。指针比较的结果基于其指向的内存地址在内存中的排列顺序。

```c
int *p1 = /* 指向某个内存地址 */;
int *p2 = /* 指向另一个内存地址 */;

if (p1 < p2) {
  // p1 所指向的内存地址在 p2 之前
} else if (p1 > p2) {
  // p1 所指向的内存地址在 p2 之后
} else {
  // p1 和 p2 指向相同的内存地址，或者 p1 和 p2 无法进行大小比较
}
```

> 指针关系运算的结果并不一定总是有意义的。只有当两个指针指向同一个数组中的元素（或指向同一个对象）时，它们之间的关系才有实际意义。
>
> 此外，还应谨慎处理指向不同对象类型的指针之间的关系比较，因为这可能会导致未定义的行为。
>
> 标准规定：C 语言允许指向数组元素的指针与指向数组最后一个元素后面的那个内存位置的指针比较，但是不允许与指向第一个元素之前的那个内存位置的指针进行比较。

#### 指针和数组

指针和数组之间存在着紧密的联系。简单来说，数组实际上就是一段连续的内存空间，而指针则是一个变量，用于存储内存地址。因此，我们可以使用指针来访问数组元素，也可以将数组名作为指针使用。如下就是一些常用的关于指针和数组的用法：

1. 使用指针访问数组元素：

```c
int arr[] = {1, 2, 3, 4, 5};
int *p = arr;  // 将数组名作为指针使用

for (int i = 0; i < 5; i++) {
  printf("%d ", *(p + i));  // 使用指针访问数组元素
}
```

> 在上面的例子中，我们定义了一个整型数组 arr，并将其首地址赋值给指针 p。然后，我们使用指针 p 来访问数组中的元素，注意到 *(p+i) 和 p[i] 是等价的。

2. 数组名作为指针使用：

```c
int arr[] = {1, 2, 3, 4, 5};

for (int i = 0; i < 5; i++) {
	// arr 指向数组的第一个位置的索引
  printf("%d ", *(arr + i));  // 数组名作为指针使用
}
```

#### 二级指针

二级指针是一个指向指针的指针，它存储了一个指针变量的地址。简单来说，二级指针就是指向指针的指针。

二级指针的定义及用法如下：

```c
#include <stdio.h>

int main() {
  int a = 10;
  int *p = &a;
  int **pp = &p; // 定义二级指针，并将一级指针 p 赋值给 pp

  printf("%d\n", **pp);  // 10

  **pp = 1209; // 通过二级指针修改 a 的值

  printf("pp = %d  a = %d\n", **pp, a);  // pp = 1209  a = 1209

  return 0;
}
```

#### 指针数组

指针数组是一个由指针组成的数组。每个元素都是指向相应类型的数据的指针。指针数组可以用于存储多个指针，并且每个指针可以指向不同类型的数据。

指针数组的定义：

```c
int *ptrArray[5];  // 定义一个指针数组，包含 5 个指针元素
```

初始化指针数组：

```c
int a = 10, b = 20, c = 30;
int *ptrArray[3] = {&a, &b, &c};  // 初始化指针数组
```

使用指针数组：

```c
#include <stdio.h>

int main() {
  int a = 10, b = 20, c = 30;
  int *ptrArray[3] = {&a, &b, &c};

  for (int i = 0; i < 3; i++) {
    printf("%d ", *(ptrArray[i]));  // 10 20 30
  }

  return 0;
}
```

> 上述代码中，`*(ptrArray[i])` 首先通过 `ptrArray[i]` 获取到指针数组中存储的三个指针变量，在通过 `*(ptrArray[i])` 解引用地址得到指针地址分别指向的变量 10、20、30。

使用指针数组实现二维数组：

```c
#include <stdio.h>

int main() {
  int arr1[4] = {1, 2, 3, 4};
  int arr2[4] = {2, 3, 4, 5};
  int arr3[4] = {3, 4, 5, 6};

  // arr1，arr2，arr3，分别是指向 arr1、arr2、arr3 的第一个元素的指针
  int* parr[3] = {arr1, arr2, arr3};

  int i = 0;

  for(i = 0; i < 3; i++) {
    int j = 0;
    // parr[i] 得到的就是 arr1、arr2、arr3
    // parr[i][j] 得到的就是 arr2、arr2、arr3 之中的每个元素
    for(j = 0; j < 4; j++) {
      printf("%d ", parr[i][j]);
    }
    printf("\n");
  }
  /*
    循环结束最终输出：
      1 2 3 4
      2 3 4 5 
      3 4 5 6 
  */

  return 0;
}
```

> 上述代码中之所以能直接通过 `parr[i][j]` 得到指针所指向的变量，是因为 `parr[i][j]` 就等价于 `*(*(parr + i) + j)`，即这里的 `[]` 就等价于解引用。

### 结构体

C 语言中的结构体（struct）是一种用户自定义的数据类型，它允许将不同类型的变量组合在一起，形成一个更复杂的数据结构。也就是说结构体的成员可以是**标量、数组、指针、甚至是其它结构体**。

#### 结构体的声明

结构体的定义使用关键字 `struct`，后跟结构体的名称和一对花括号 `{}`，在花括号内部定义结构体的成员。每个成员由其类型和名称组成，类似于变量的声明。具体写法如下：

```c
// 定义一个名为 Student 的结构体，包含姓名、年龄和体重三个数据成员
struct Student {
  char name[20];
  int age;
  float weight;
};

// 将其它结构体作为类型放入结构体中
struct Person {
  struct Student std;
  float phone;
};
```

> Student 是一个结构体类型，不占用内存空间。

初始化结构体变量：

```c
// stu 是结构体变量，声明时会向内存中申请空间
struct Student stu = {"dnhyxc", 18, 70.2};  // 初始化一个名为 stu 的结构体变量

struct Person per = {{"dnhyxc", 18, 70.2}, 18866669999};
```

访问结构体成员：

```c
#include <stdio.h>

// 定义一个名为 Student 的结构体，包含姓名、年龄和体重三个数据成员
struct Student {
  char name[20];
  int age;
  double weight;
};

// 将其它结构体作为类型放入结构体中
struct Person {
  struct Student std;
  long phone;
};

void printStu(struct Student stu) {
  printf("%s %d %.1f\n", stu.name, stu.age, stu.weight); // hmhm 18 41.9
}

void printPer(struct Person* per) {
  printf("%s %d %.1f %ld\n", per->std.name, per->std.age, per->std.weight, per->phone); // dnhyxc 18 70.2 18866669999
}

int main() {
  struct Student stu = {"hmhm", 18, 41.9};
  struct Person per = {{"dnhyxc", 18, 70.2}, 18866669999};

  printf("name: %s\n", stu.name); // name: hmhm
  printf("age: %d\n", stu.age); // age: 18
  printf("weight: %.1f\n", stu.weight); // weight: 41.9

  printf("%s %d %.1f %ld\n", per.std.name, per.std.age, per.std.weight, per.phone); // dnhyxc 18 70.2 18866669999

  // 传入结构体变量
  printStu(stu);

  // 传入结构体地址
  printPer(&per);

  return 0;
}
```

> 如果获取到的是一个结构体的地址，那么访问结构体成员时可以使用 `->` 进行访问，如：`stu.name` 就可以改写为 `stu->name`。

#### 结构体传参

结构体传参有两种形式，分别是：

1. 传递结构体变量：

```c
#include <stdio.h>

// 定义一个名为 Student 的结构体，包含姓名、年龄和体重三个数据成员
struct Student {
  char name[20];
  int age;
  double weight;
};

void printStu(struct Student stu) {
  printf("%s %d %.1f\n", stu.name, stu.age, stu.weight); // hmhm 18 41.9
}

int main() {
  struct Student stu = {"hmhm", 18, 41.9};

  // 传入结构体变量
  printStu(stu);

  return 0;
}
```

2. 传递结构体指针：

```c
#include <stdio.h>

// 定义一个名为 Student 的结构体，包含姓名、年龄和体重三个数据成员
struct Student {
  char name[20];
  int age;
  double weight;
};

// 将其它结构体作为类型放入结构体中
struct Person {
  struct Student std;
  long phone;
};

void printPer(struct Person* per) {
  printf("%s %d %.1f %ld\n", per->std.name, per->std.age, per->std.weight, per->phone); // dnhyxc 18 70.2 18866669999
}

int main() {
  struct Person per = {{"dnhyxc", 18, 70.2}, 18866669999};

  // 传入结构体地址
  printPer(&per);

  return 0;
}
```

> 函数传参的时候，参数需要压栈，如果传递一个结构体对象的时候，结构体过大，参数压栈的系统开销就会比较大，所以会导致心能下降。因此结构体传参的时候，尽量传递结构体地址。

### 语句

前言：C 语言语句可以分为五类，分别是：**控制语句**、**表达式语句**、**函数调用语句**、**复合语句**、**空语句**。

### 控制语句

控制语句是用于控制程序执行流程，以实现程序的各种结构方式，它们由特定的语句定义符组成，C 语言有九种控制语句，大体可以分为以下三类：

- 条件判断语句，同时也叫分支语句：`if 语句`、`switch 语句`。

- 循环执行语句：`do while 语句`、`while 语句`、`for 语句`。

- 转向语句，也叫跳转语句：`break 语句`、`goto 语句`、`continue 语句`、`return 语句`。

#### 分支语句（选择结构）

if 语句：用于基于条件的真假来执行不同的代码块。基本结构如下：

```c
// 单条件
if (condition) {
  // 如果条件为真，则执行这里的代码
}

// 多条件
if (condition) {
  // 如果条件为真，则执行这里的代码
} else {
  // 如果条件为假，则执行这里的代码
}

// 更多条件
if (condition1) {
  // 如果条件1为真，则执行这里的代码
} else if (condition2) {
  // 如果条件2为真，则执行这里的代码
} else {
  // 如果以上条件都不满足，则执行这里的代码
}

// 使用示例
#include "stdio.h"

int main() {
	int age = 21;

	if (age < 18) {
		printf("未成年\n");
	} else if (age > 18 && age <= 35) {
		printf("正值青年\n");
	} else if (age > 35 && age <= 55) {
		printf("正值中年\n");
	} else {
		printf("开始步入老年生活了\n");
	}

	return 0;
}
```

> 说明：在 C 语言中，0 表示假，非 0 表示真。`else` 是离他最近的一条 `if` 语句相匹配。

#### switch 语句

switch 语句也是一种分支语句，常用于多分支的情况，基本结构如下：

```c
switch (expression) {
  // case 必须是整形常量表达式
  case value1:
    // 如果expression等于value1，则执行这里的代码
    break;
  case value2:
    // 如果expression等于value2，则执行这里的代码
    break;
  default:
    // 如果expression不匹配任何case，则执行这里的代码
    break;
}

// 使用示例
#include "stdio.h"

int main() {
  
  int day = 1;

  switch (day) {
    case 1:
      printf("星期一\n");
      break;
    case 2:
      printf("星期二\n");
      break;
    case 3:
      printf("星期三\n");
      break;
    case 4:
      printf("星期四\n");
      break;
    case 5:
      printf("星期五\n");
      break;
    case 6:
      printf("星期六\n");
      break;
    case 7:
      printf("星期天\n");
      break;
    default:
      printf("没有找到一个匹配的，就会走到这，\n");
      break;
  }

  return 0;
}
```

如果想要给多个 `case` 执行同一个效果时，可以省略 `break`，具体写法如下：

```c
#include "stdio.h"

int main() {

	int day = 6;

	switch (day) {
		case 1:
		case 2:
		case 3:
		case 4:
		case 5:
			printf("又是搬砖的一天，星期%d\n", day);
			break;
		case 6:
		case 7:
			printf("今天终于不用搬砖了，星期%d\n", day);
			break;
		default:
      printf("没有找到一个匹配的，就会走到这，%d\n", day);
			break;
	}

	return 0;
}
```

switch 语句是可以嵌套的，其中嵌套的 switch 中的 `break` 只会跳出自身的 switch，而不会跳出外层的 switch：

```c
int main() {
  int n = 1;
  int m = 2;

  switch (n) {
    case 1:
      m++;
    case 2:
      n++;
    case 3:
      switch (n) {
        case 1: 
          n++;
        case 2: 
          m++;
          n++;
          break; // 跳出嵌套的 switch
      }
    case 4:
      m++;
      break;
    default:
      break;
  }

  printf("m = %d, n = %d\n", m, n); // m = 5, n = 3

  return 0;
}
```

####  while 循环语句

C 语言中的 while 循环是一种常用的循环结构，它会**重复执行**一段代码，直到给定的条件为假为止。其基本语法结构如下：

```c
// condition 条件为真（非零）进入循环，为假（0）则跳出循环
while (condition) {
  // 需要重复执行的代码
}
```

condition：是一个表达式，当其值为真（非零）时，循环会继续执行。一旦 condition 的值为假（0），循环将停止，并继续执行循环后面的代码，具体执行流程如下：

![image.png](http://43.143.27.249/image/56607990af96ba2563bafcf0899ad87a.png){{{width="100%" height="auto"}}}

**说明**：上图中 `break` 将永久终止循环，即直接跳出整个循环，而 `continue` 则是只跳出本次循环，即本次循环中 continue 之后的代码将不被执行，会直接到 while 循环的判断部分，继续执行本次循环之后满足条件的循环。

while 循环基本使用示例：

```c
#include <stdio.h>

int main() {
  int i = 1;
  // 当 i 大于 5 时，条件不满租，将跳出循环
  while (i <= 5) {
    printf("%d\n", i);
    i++;
  }

  printf("while 外层 i = %d\n", i);
  return 0;
}
```

**注意**：在使用 while 循环时，一定要确保循环体内的代码能够使循环的条件最终变为假，否则可能导致无限循环的情况。

使用 `break` 跳出循环示例：

```c
#include <stdio.h>

int main() {
  int i = 1;
  // 当 i 大于 5 时，条件不满租，将跳出循环
  while (i <= 10) {
    i++;
    // 当 i 等于 5 时，直接跳出整个循环
    if (i == 5) break;
    printf("%d\n", i); // 2 3 4
  }

  return 0;
}
```

使用 `continue` 跳出本次循环示例：

```c
#include <stdio.h>

int main() {
	int i = 1;
	// 当 i 大于 5 时，条件不满租，将跳出循环
	while (i <= 10) {
		i++;
    // i 等于 5 时，跳出本次循环，直接执行下一次循环
		if (i == 5) continue;
    // i++; 如果将 i++ 放在 continue 的后面, 会导致死循环
		printf("%d\n", i); // 2 3 4 6 7 8 9 10 11
	}

	return 0;
}
```

**注意**: 如果将 i++ 放在 continue 的后面，会导致死循环。

#### for 循环语句

C 语言中的 for 循环是一种常用的循环结构，它会重复执行一段代码，可以很方便地控制循环次数。其基本的语法结构如下：

```c
for (initialization; condition; update) {
  // 需要重复执行的代码
  循环体语句;
}
```

参数说明：

- initialization：表示初始化表达式，是循环开始时执行的一条语句，通常用于初始化一个计数器变量。

- condition：表示循环条件表达式，是一个表达式，当其值为真（非零）时，循环会继续执行。

- update：表示更新表达式，在每次循环结束后执行的一条语句，通常用于更新计数器变量的值。循环体内的代码将在每次循环开始时执行，直到 condition 的值为假（0），循环将停止，并继续执行循环后面的代码。

- 循环体语句：循环的核心部分，可以是任意数量的语句。

for 循环基本使用示例：

```c
#include <stdio.h>

int main() {
  int sum = 0;
  for (int i = 1; i <= 10; i++) {
    sum += i;
  }
  printf("1 + 2 + ... + 10 = %d\n", sum);
  return 0;
}
```

上述代码大致执行流程如下：

![image.png](http://43.143.27.249/image/edb73d97f0b822999a3e61d27108f5de.png){{{width="100%" height="auto"}}}

在上图中，for 循环中的 `break` 和 `continue` 与 while 循环中的 break 和 continue 效果基本是一致的，但是对于 continue 稍微存在一点差异，为了能清晰的看出差异，直接上一段代码：

```c
// 使用 break 跳出整个循环
#include <stdio.h>

int main() {
  int i = 0;
  for(i = 1; i <= 10; i++) {
    if(i == 5) {
      break;
    }
    printf("%d\n", i)
  }

  return 0;
}

// 使用 continue 跳出本次循环
#include <stdio.h>

int main() {
  int i = 0;
  for(i = 1; i <= 10; i++) {
    if(i == 5) {
      continue;
    }
    printf("%d\n", i)
  }

  return 0;
}
```

**说明**：上述代码中，break 和 while 循环中的效果是一致的，但是对于 continue，区别就在于 while 循环中的 continue 跳过本次循环时，如果将 `i++` 放在 continue 之后，将会导致死循环，而对于 for 循环，由于 for 循环的执行机制，`i++` 在循环体运行结束之后才会执行，所以即使 continue 跳出了本次循环，也不会导致死循环。

下面是一道 for 循环面试题，问：该 for 循环会循环多少次？

```c
#include <stdio.h>

int main() {
  int i = 0;
  int k = 0;
  for(i = 1, k = 0; k = 0; i++) {
    k++;
    printf("%d\n", i);
  }
  printf("循环结束\n");
  return 0;
}
```

> 答案是 *（如果不太肯定，放编辑器跑一下吧），原因是因为其中控制语句为 `k = 0`，是一个赋值语句，k 等于 0，条件为假，因此条件始终不成立（for 循环条件不等于 0 时，条件为真，等于 0 时，条件为假），因此该循环的循环结果是：循环 0 次。

#### do while 循环语句

do while 循环会重复执行一段代码，直到给定的条件为假为止。和 while 循环相比，**do while 循环至少会执行一次循环体内的代码**，基本语法结构如下：

```c
do {
  // 需要重复执行的代码
} while (condition);
```

condition：是一个表达式，当其值为真（非零）时，循环会继续执行。一旦 condition 的值为假（0），循环将停止，并继续执行循环后面的代码，执行流程如下图所示：

![image.png](http://43.143.27.249/image/16a56d0c2caa36d6775a017f91d432fa.png){{{width="100%" height="auto"}}}

**说明**：do while 循环中，`break` 和 `continue` 的作用与 while 循环中是一致的，与 while 循环中将 `i++` 放在 continue 之后一样，也会造成死循环。因此，为了避免造成死循环，建议把 `i++` 放在 continue 之前。

#### 循环语句总结

`for` 循环适用于已知循环次数的情况，`while` 和 `do-while` 循环适用于未知循环次数的情况。在使用时需要根据具体需求选择合适的循环结构。其中要注意的是，`while` 和 `do-while` 循环中使用 `continue` 时，如果有 `i++`，需要将其写在 continue 前面，防止死循环的发生。

### 函数

C 语言函数是一种可重复使用的代码块，用于实现特定任务或功能。它可以接受参数、执行操作，并返回结果。函数在 C 语言中起到了**模块化编程**和**代码重用**的重要作用。

在 C 语言中，函数分为**库函数**和**自定义函数**，这两类函数在下文中将会着重介绍。

### 库函数

库函数是 C 语言中提供的一些公共函数，只需要在我们的代码文件中导入对应的头文件即可使用对应的库函数，方便我们更方便的开发。

在 C 语言中，常用的标准头文件有一下几类：

- <stdio.h>：提供了一些输入输出函数。

- <stdlib.h>：包含了通用实用工具函数。

- <string.h>：包含了字符串处理函数。

- <math.h>：提供了数学计算函数。

- <ctype.h>：包含了字符分类和转换函数。

- <time.h>：提供了时间和日期操作函数。

- <assert.h>：包含了断言宏定义，用于在调试阶段进行条件检查。

- <stdbool.h>：定义了 bool 类型和 true、false 常量。

C 语言库函数官方文档：

[cppreference 英文版](https://en.cppreference.com/w/c/header)

[cppreference 中文版](https://zh.cppreference.com/w/c/header)

#### <stdio.h>

|函数原型|功能|
|-|-|
|[int printf(char *format...)](https://www.runoob.com/cprogramming/c-function-printf.html)|产生格式化输出的函数|
|[int getchar(void)](https://www.runoob.com/cprogramming/c-function-getchar.html)|从键盘上读取一个键，并返回该键的键值|
|[int putchar(int char)](https://www.runoob.com/cprogramming/c-function-putchar.html)|把参数 char 指定的字符（一个无符号字符）写入到标准输出 stdout 中。|
|[FILE *fopen(const char *filename, const char *mode)](https://www.runoob.com/cprogramming/c-function-fopen.html)|使用给定的模式 mode 打开 filename 所指向的文件。|
|[FILE *freopen(const char *filename, const char *mode, FILE *stream)](https://www.runoob.com/cprogramming/c-function-freopen.html)|把一个新的文件名 filename 与给定的打开的流 stream 关联，同时关闭流中的旧文件。|
|[int fflush(FILE *stream)](https://www.runoob.com/cprogramming/c-function-fflush.html)|刷新流 stream 的输出缓冲区。|
|[int fclose(FILE *stream)](https://www.runoob.com/cprogramming/c-function-fclose.html)|关闭流 stream。刷新所有的缓冲区。|
|[void clearerr(FILE *stream)](https://www.runoob.com/cprogramming/c-function-clearerr.html)|清除给定流 stream 的文件结束和错误标识符。|
|[int feof(FILE *stream)](https://zh.cppreference.com/w/c/io/feof)|检查给定流 stream 的文件结束标识符。|

### 自定义函数

由于库函数是有限的，库函数无法解决我们所有的问题，因此为了能够有效的解决我们所遇到的问题，就需要我们自己定义函数。而这就是自定义函数，即通过我们自己定义的函数。

自定义函数和库函数一样，由**函数名**，**返回值类型**和**函数参数**（参数可有可无，视情况而定）组成。函数的基本定义如下：

```c
返回类型 函数名(参数列表) {
  // 函数体
}
```

- 返回类型：指定了函数返回值的数据类型，可以是整数、浮点数、指针等。

- 函数名：函数的标识符，用于在程序中调用该函数。

- 参数列表：列出了函数接受的参数，每个参数由参数类型和参数名组成，多个参数之间用逗号分隔。

- 函数体：包含了函数执行的具体代码。

#### 函数的形参和实参

形式参数（形参）：

- 自定义函数接收的参数列表称之为形式参数，简称**形参**。

- 因为形式参数只有在函数被调用的过程中才实例化，因此在声明形参时不会申请存储空间，只有在函数调用时才会申请存储空间。

- 形式参数当函数调用完成之后就会自动销毁，因此形式参数只在当前声明该形参的函数中有效。

实际参数（实参）：

- 在调用自定义函数时，给自定义函数传入的实际参数称之为**实参**。

- 实参可以是：常量、变量、表达式或函数等。

- 无论实参是何种类型的量，在进行函数调用时，它们都必须有确定的值，以便把这些值传送给形参。

```c
// 这里 a 和 b 就是形参
int CustomFn(int a, int b) {
  // 函数体
}

int main() {
  int a = 1101;
  int b = 1209;

  // 这里调用 CustomFn 函数时传入的 a 和 b 就是实参
  const res = CustomFn(a, b);
  return 0;
}
```

#### 函数的调用

传值调用：

- 函数的形参和函数的实参分别占有不同的内存，对形参的修改不会影响实参。

传址调用：

- 传址调用是把函数外部创建变量的内存地址传递给函数形参的一种调用方式。

- 这种传参方式可以让函数和函数外的变量（可以理解为形参和实参）建立真正的联系，也就是函数内部可以直接操作函数外部的变量。


#### 函数的声明和定义

函数的声明：

- 函数的声明可以告诉编译器，函数叫什么，参数是什么，返回类型是什么，防止在调用函数时编译器报“xxx函数未定义”的警告。

- 函数是不是存在，通过函数声明无法决定。

- 函数的声明一般出现在函数的使用之前，要满足**先声明后使用**的原则。

- 函数的声明一般要放在头文件中。

函数的定义：

- 函数的定义是指函数的具体实现，交代函数的具体功能实现。

如果要在调用之后再定义函数，就需要现在调用之前先声明函数，具体实现方式如下：

```c
#include <stdio.h>

// 函数声明
int Add(int a, int b);

int main() {
  int a = 12;
  int b = 9;

  int sum = Add(a, b);

  printf("%d\n", sum);

  return 0;
}

// 定义函数
int Add(int a, int b) {
  return a + b;
}
```

上述代码中，函数的声明和定义都写在同一个文件中，除了上述的方式，我们还可以将函数的生命放在特定的头文件中，将函数的定义放在对应的函数定义文件夹中，如：

- 在项目头文件夹中创建 `add.h` 的文件，在该文件中声明函数：

```c
// 定义 Add 求和函数
int Add(int a, int b);
```

- 在项目源文件中增加 `add.c` 文件，在该文件中定义函数：

```c
int Add(int a, int b) {
  return a + b;
}
```

- 在 `main.c` 文件中的主函数 `main` 中导入函数声明，并调用 `Add` 函数：

```c
#include <stdio.h>

// 导入 add.h 中声明的求和函数声明
#include "add.h"

int main() {
	int a = 12;
	int b = 9;

	// 调用 add.c 中定义的求和函数
	int sum = Add(a, b);

	printf("%d\n", sum);

	return 0;
}
```

> 在上述主函数中，并没有声明及定义 `Add` 函数，但通过 `#include "add.h"` 导入 `Add` 函数的头文件之后，即可调用 `add.c` 中定义的 `Add` 函数了。通过这种方式可以根据业务对代码进行拆分，使每个文件都对应每个特定的需求，最终可以将每个功能汇总到主函数中，利益代码的维护及团队协作。

#### 自定义函数定义示例

1. 定义一个自定义函数，计算两个数的和：

```c
#include <stdio.h>

int Add(int a, int b) {
	return a + b;
}

int main() {
	int a = 12;
	int b = 9;

	int sum = Add(a, b);

	printf("%d\n", sum); // 21

	return 0;
}
```

2. 定义一个函数，用于交换两个整形变量的值：

```c
#include <stdio.h>

void Swap(int x, int y) {
	printf("交换前: x=%d y=%d\n", x, y); // 交换前: x=12 y=9

	int temp = 0;
	temp = x;
	x = y;
	y = temp;
}

int main() {
	int a = 12;
	int b = 9;

	Swap(a, b);

	printf("交换后: a=%d b=%d\n", a, b); // 交换后: a=12 b=9

	return 0;
}
```

**说明**：执行上述 `Swap` 函数之后，发现并没有达到交换两个数的值的效果。这是因为，`Swap` 函数的形参 `x` 和 `y` 开辟了自己的存储空间，也就是说，形参 `x` 和 `y` 与实参 `a` 和 `b` 都有自己单独的存储地址，即形参 `x, y` 与实参 `a, b` 没有任何关联，因此，即使在 `Swap` 中交换了 `x, y` 的值，也不会影响实参 `a, b` 的值，这仅仅交换了 `x, y` 的值。

> **总结**：当实参传递给形参的时候，形参是实参的一份临时拷贝，对形参的修改不会影响实参。

要想达到正真的交换效果，可以通过以下几种方式解决：

1. 传递指针参数的方式：

```c
#include <stdio.h>

void Swap(int* x, int* y) {
	printf("交换前: x=%d y=%d\n", *x, *y); // 交换前: x=12 y=9

	int temp = 0;
	temp = *x;
	*x = *y;
	*y = temp;
}

int main() {
	int a = 12;
	int b = 9;

	Swap(&a, &b);

	printf("交换后: a=%d b=%d\n", a, b); // 交换后: a=9 b=12

	return 0;
}
```

> 上述代码中，通过传递 `a, b` 的指针给形参 `x, y`，使 `x, y` 与 `a, b` 建立联系，达到交换 `a, b` 的值的效果。这种情况下，虽然形参 `x, y` 也会开辟自己的存储空间，但是开辟的空间中存的是 `a, b` 的地址（指针），而通过这个地址就能准确的找到 `a, b`，从而通过指针交换 `a, b` 的值。

2. 通过按位异或（^）操作符实现，但需要注意的是，该方式只适用于整数，对于浮点数不适用：

```c
#include <stdio.h>

int main() {
	int a = 12; // 1100
	int b = 9;  // 1001 => 0101

	printf("交换前: a=%d b=%d\n", a, b); // 交换后: a=12 b=9

	a = a ^ b; // 12 ^ 9 => 5
	printf("a=%d\n", a); // 5

	b = a ^ b; // 12 ^ 9 ^ 9 => 12
	printf("b=%d\n", b); // 12

	a = a ^ b; // 12 ^ 9 ^ 12 => 9
	printf("a=%d\n", a); // 9

	printf("交换后: a=%d b=%d\n", a, b); // 交换后: a=9 b=12

	return 0;
}
```

> **说明**：
> 
> 1. 两个相同的数按位异或为 0。
> 
> 2. 0 和任何一个整数按位异或为该整数。
> 
> ```c
> #include <stdio.h>
> 
> int main() {
> 	int a = 12;
>   int b = 12;
>   int c = a ^ b;
>   printf("%d\n", c); // 0
>   
>   int _a = 0;
>   int _b = 12;
>   int _c = _a ^ _b;
>   printf("%d\n", _c); // 12
> 
> 	return 0;
> }
> ```

#### 函数的嵌套调用

函数的嵌套调用是指在一个函数内部调用另一个函数，并且被调用函数内部也可以继续调用其他函数。这种嵌套结构可以让程序更加模块化和灵活，可以将复杂的任务划分成多个独立的子任务，每个子任务由一个函数负责完成，从而提高代码的可读性和可维护性。

**注意**：函数可以嵌套调用，但是不可以进行嵌套声明。

函数的嵌套调用示例：

```c
#include <stdio.h>

int add(int a, int b) {
	return a + b;
}

int multiply(int a, int b) {
	return a * b;
}

void compute() {
	int a = 12;
	int b = 9;
	int c = 0;
	int d = 0;

	c = add(a, b);
	d = multiply(a, b);

	printf("%d + %d = %d\n", a, b, c); // 12 + 9 = 21 
	printf("%d * %d = %d\n", a, b, d); // 12 * 9 = 108
}

int main() {
	compute();

	return 0;
}
```

在上述代码中，main 函数调用了 compute 函数，而在 compute 中调用了两个其他函数 add 和 multiply，这两个函数分别用于计算两个数的和和积。add 函数返回两个数的和，multiply 函数返回两个数的积。compute 函数通过调用这两个函数来计算并输出结果。

在这个例子中，add 和 multiply 函数被嵌套在 compute 函数内部，但它们也可以调用其他函数。这种嵌套结构可以在复杂的程序中发挥巨大的作用，让程序更加模块化和易于管理。

> 需要注意的是，函数的嵌套调用可能会导致调用栈溢出的问题。如果函数的嵌套层数太深，调用栈可能会超过系统所允许的最大深度，从而导致程序崩溃。因此，在编写程序时，需要注意函数的嵌套深度，避免出现调用栈溢出的问题。

#### 函数的链式调用

C 语言函数的链式调用是指将多个函数的返回值依次传递给下一个函数，实现类似链表的操作。

链式调用通常用于处理大量数据或需要逐个处理数据的情况。

函数的链式调用示例：

```c
#include <stdio.h>

int add(int a, int b) {
	return a + b;
}

int main() {
	int a = 12;
	int b = 9;

	// 链式调用
	int sum = add(a, add(a, add(a, add(a, add(a, b)))));

	printf("%d ", sum); // 69

	return 0;
}
```


### 函数递归

程序调用自身的编程技巧称之为**递归**。它作为一种算法在程序设计语言中被广泛使用。

递归，指函数在其定义或说明中有直接或间接调用自身的一种方法，它通常把一个大型复杂的问题层层转化为一个与原问题相似的规模大小的问题来求解。

递归策略只需少量的程序就可描述出接替过程所需的多次重复计算，大大较少了程序的代码量。

递归的主要思考方式在于：大事化小。

#### 递归的两个必要条件

1. 存在限制条件，当满足这个限制条件的时候，递归就不再继续。

2. 每次递归调用之后越来越接近这个限制条件。

#### 递归的使用示例

1. 接受一个整型值（无符号），按照顺序打印它的每一位，如：输入 12345，输出 54321。

```c
#include <stdio.h>

// 函数声明
int Print(unsigned int n);

int main() {
	int a = 1234;
	Print(a);
	return 0;
}

// 函数定义
int Print(unsigned int n) {
	// 12345
	// 1234
	// 123
	// 12
	// 1
	printf("%d\n", n);

	if (n > 9) {
		Print(n / 10);
	}

	printf("%d", n % 10); // 12345
}
```

上述代码执行流程图如下：

![image.png](http://43.143.27.249/image/a9e2e020ba15acc47a21b9fda2f9e3c2.png){{{width="100%" height="auto"}}}

2. 字符串逆序：

- 使用 `while` 循环实现：

```c
#include <stdio.h>
#include <string.h>

void reverseStr(char str[]) {
	int left = 0;

	// 计算方式1，因为索引是从 0 开始，并且 sz 包含了 \n 的长度，因此要减去 2
	//int right = sizeof(str) / sizeof(str[0]) - 2;

	// 计算方式二
	int right = strlen(str) - 1;

  // 当 left 大于等于 right 时，说明字符串全部调换完毕，退出循环
	while (left < right) {
    // 利用中间量调换左右字符
		char temp = str[left];
    // 将右字符调换为左字符
		str[left] = str[right];
    // 将左字符调换为右字符
		str[right] = temp;

		left++;

		right--;
	}

	printf("%s\n", str);
}

int main() {
	char str[] = "dnhyxc"; // [d n h y x c \n]

	reverseStr(str);

	return 0;
}
```

- 使用递归实现（方式一）：

```c
#include "stdio.h"
#include "string.h"

void reverseStr(char str[], int left, int right) {
  if (left < right) {
    char temp = str[left];
    str[left] = str[right];
    str[right] = temp;
    reverseStr(str, left+1, right-1);
  }
}

int main() {
  char str[] = "dnhyxc"; // [d n h y x c \n]
  int left = 0;
  int right = strlen(str) - 1;
  reverseStr(str, left, right);
  printf("%s", str);
  return 0;
}
```

- 使用递归实现（方式二）：

```c
#include "stdio.h"

// 实现字符串长度计算函数
int myStrlen(char *str) {
  int count = 0;
  while(*str != '\0') {
    count++;
    str++;
  }
  return count;
}

void reverseStr(char *str) {
  char temp = *str;
  int len = myStrlen(str);
  // 将数组第一个替换成数组最后一个的值
  *str = *(str + len - 1);
  // 将数组最后一位先填充为'\0'，方便后续将数组倒数第二个替换到数组第一个去
  *(str + len - 1) = '\0';
  // 判断数组长度是否大于等于2，如果是则说明还需要继续替换
  if (myStrlen(str + 1) >=2) {
    // 使用递归继续替换剩下的
    reverseStr(str + 1);
  };
  // 替换完成后，将最后一个填充为之前替换成'\0'的元素
  *(str + len - 1) = temp;
}

int main() {
  char str[] = "dnhyxc";
  reverseStr(str);
  printf("%s\n", str);

  return 0;
}
```

### 隐式类型转换

#### 整型提升

当一个较小的整型类型与较大的整型类型混合运算时，较小的整型类型会被自动提升为较大的整型类型。例如，int 类型和short 类型进行运算时，short 类型会被提升为 int 类型。

1. 为什么会进行整型提升？

- C 语言中的整型算术运算总是以默认的整型类型的精度来进行的，为了获得这个精度，表达式中的字符和短整型操作数在使用之前就会被转换为普通整型。

- 表达式的整型运算要在 CPU 的相应运算器件内执行，CPU 内整型运算器（ALU）的操作数的字节长度一般就是 int 的字节长度，同时也是 CPU 的通用寄存器的长度，因此，即使两个 char 类型相加，在 CPU 执行时实际也要先转换为 CPU 内整型操作数的标准长度。

- 通用 CPU（general-purpose CPU）是难以直接实现两个 8 bit 字节进行相加运算的（虽然机器指令中可能有这种字节相加指令）。所以表达式中各种长度可能小于 int 长度的整型值，都必须先转换为 int 或 unsigned int，然后才能送入 CPU 中执行运算。

2. 整型提升的意义：

- **避免精度丢失**：整型提升可以避免由于不同整数类型的运算导致的精度丢失。例如，将一个 char 类型和一个 int 类型相加时，char 类型的值会被自动提升为 int 类型，以保留较大整数类型的精度。

- **扩展整数范围**：整型提升可以将较小的整数类型扩展为较大的整数类型，以确保运算结果不会溢出。例如，将一个 short 类型和一个 int 类型相加时，short 类型的值会被自动提升为 int 类型，以保证运算结果在 int 类型的范围内。

- **与默认整数类型匹配**：整型提升确保操作数具有相同的类型，以与默认整数类型匹配。这样可以简化编译器的实现，并提高代码的可移植性。例如，将一个 short 类型和一个 long 类型进行运算时，short 类型会被提升为 long 类型，以与默认的 long 类型匹配。

3. 如何进行整型提升？

整型提升是按照变量的数据类型的符号位来提升的：

- 负数的整型提升：声明一个变量 `char c1 = -1;`，其中变量 c1 的二进制位（补码）中只有 8 个比特位：`11111111`，因为 char 为有符号的 char，所以整型提升的时候，高位补充符号位即为 1，因此提升之后的结果为：`11111111111111111111111111111111`。

- 正数的整型提升：声明一个变量 `char c2 = 1;`，其中变量 c2 的二进制位（补码）中只有 8 个比特位：`00000001`，因为 char 为有符号的 char，所以整型提升的时候，高位补充符号位即为 0，因此提升之后的结果为：`00000000000000000000000000000001`。

- 无符号整型提升：高位直接补充 0。

```c
#include "stdio.h"

// 整型提升实例一
void test1() {
	// 00000000000000000000000000000101 原码
	char a = 5; // a 是有符号 char 类型的数字在内存中存的就是 00000101

	// 00000000000000000000000001111110 原码
	char b = 126; // b 是有符号 char 类型的数字在内存中存的就是 01111110

	// 触发整型提升
	/*
		a，b 是正数，所以原码和补码一样。
		00000000000000000000000000000101（a） + 00000000000000000000000001111110（b）
		=> 00000000000000000000000010000011（补码）。

		c 是有符号 char 类型的数字在内存中存储时，补码会被截断成 1 个字节，也就是 8 bit，
		因此 c 在内存中存储的就是 10000011。
	*/
	char c = a + b;  // 10000011

	/*
		由于打印的是一个整型，因此 c 会触发整型提升，10000011 的高位为 1，
		因此高位补充 1，得到 11111111111111111111111111000011（存储在内存中的 c 的补码）。

		打印的 c 应该是原码，因此先要将 11111111111111111111111111000011 减去 1，得到 c 的反码：
		11111111111111111111111111000010，再将得到的反码转为源码（除符号位之外，其它位取反），得到：
		10000000000000000000000000111101（-125），因此 a + b 得到的 c 就为 -125。
	*/
	printf("%d\n", c); // -125
}

// 整型提升示例二
void test2() {
	char a = 0xb6;
	short b = 0xb600;
	int c = 0xb6000000l;

	if (a == 0xb6) {
		printf("a");
	}

	if (b == 0xb600) {
		printf("b");
	}

	if (c == 0xb6000000l) {
		printf("c");
	}
}

// 整型提升实例三
void test3() {
	char c = 1;

	printf("%u\n", sizeof(c)); // 1
	// +c 触发整型提升
	printf("%u\n", sizeof(+c)); // 4
	// -c 触发整型提升
	printf("%u\n", sizeof(-c)); // 4
}

int main() {
	test1(); // -125

	test2(); // c

	test3();

	return 0;
}
```

#### 浮点数提升

当一个较小的浮点数类型与较大的浮点数类型混合运算时，较小的浮点数类型会被自动提升为较大的浮点数类型。例如，float 类型和 double 类型进行运算时，float 类型会被提升为 double 类型。

#### 整型转换

当一个整型类型赋值给另一个较小的整型类型或进行混合运算时，编译器会自动将较大的整型类型转换为较小的整型类型。这**可能导致截断或溢出**。例如，将一个 long 类型的值赋给一个 int 类型的变量时，long 类型的值会被截断为 int 类型。

#### 浮点数转换

当一个浮点数类型赋值给另一个较小的浮点数类型或进行混合运算时，编译器会自动将较大的浮点数类型转换为较小的浮点数类型。这可能导致精度丢失。例如，将一个 double 类型的值赋给一个 float 类型的变量时，double 类型的值会被转换为 float 类型。

#### 混合类型运算

当不同类型的操作数进行运算时，编译器会自动进行类型转换，将操作数转换为相同的类型。具体的转换规则由 C 语言标准定义，并且可能因编译器的实现而有所差异。

通常基本的转换原则是：

1. 占用内存字节数少（值域小）的类型，向占用内存字节数多（值域大）的类型转换，以保证精度不降低。

2. 转换方向如下图所示：

![image.png](http://43.143.27.249/image/883fe87ec093e4d453eab8be76f83e61.png){{{width="100%" height="auto"}}}

发生类型转换的几种情况：

1. 当表达式中出现了 char、short int、int 类型中的一种或者多种，没有其他类型了，参加运算的成员全部变成 int 类型的参加运算，结果也是 int 类型的：

```c
#include <stdio.h>

int main() {
  short a = 5;
  int b = 2;
  printf("%d\n", a / b); // 2
  return 0;
}
```

2. 当表达式中出现了带小数点的实数，参加运算的成员全部变成 double 类型的参加运算，结果也是 double 型：

```c
#include <stdio.h>

int main() {
	double a = 5.0;
	int b = 2;
	printf("%lf\n", a / b); // 2.500000
	return 0;
}
```

3. 当表达式中有有符号数和无符号数，参加运算的成员变成无符号数参加运算结果也是无符号数（表达式中无实数）：

```c
#include<stdio.h>

int main() {
	int a = -8;
	unsigned int b = 7;

	if (a + b > 0) {
		printf("a+b>0\n"); // a+b>0
	} else {
		printf("a+b<=0\n");
	}

	printf("(a + b) x = %x\n", (a + b)); // ffffffff
	printf("(a + b) d = %d\n", (a + b)); // -1

	return 0;
}
```

4. 在赋值语句中等号右边的类型自动转换为等号左边的类型：

```c
#include <stdio.h>

int main() {
	int a;
	// 5.8 后面加 f 代表 5.8 是 float 类型，不加的话，认为是 double 类型 
	float b = 5.8f;
	a = b;
	printf("a=%d\n", a); // a = 5

	return 0;
}
```

5. 自动类型转换都是在运算的过程中进行临时性的转换，并不会影响自动类型转换变量的值和其类型：

```c
#include<stdio.h>

int main() {
	int a;
	float b = 5.8f;
	a = b;
	printf("a=%d\n", a); // 5
	// b 的类型依然是 float 类型的，它的值依然是 5.8，0.1f 表示保留一位小数
	printf("b=%0.1f\n", b); // 5.8

	return 0;
}
```

> **总结**：
> 
> - 当进行类型提升时，总是将小类型提升为大类型，即小变大。
>
> - 当进行类型转换时，总是将大类型转换为小类型，即大转小。

**警告**：如果自己进行类型转换需要注意是否会导致精度丢失的问题如：

```c
float f = 3.14;
int num = f; // 这里会触发隐式类型转换，会导致精度丢失
```

### 表达式求值

#### 操作符的属性

复杂表达式的求值有三个影响因素：

1. 操作符的优先级。

2. 操作符的结合性。

3. 是否控制求值顺序。

> 两个相邻的操作符先执行哪个，取决于它们的优先级，如果两者的优先级相同，则看两者的结合性。

|顺序|操作符|描述|用法示例|结果类型|结合性|是否控制求值顺序|
|-|-|-|-|-|-|-|
|1|()|数组|(表达式)|与表达式同|N/A|否|
|2|()|函数调用|rexp(rexp, ...rexp)|rexp|L-R|否|
|3|[]|下标引用|rexp[rexp]|lexp|L-R|否|
|4|.|访问结构成员|lexp.memner_name|lexp|L-R|否|
|5|->|访问结构指针成员|lexp->memner_name|lexp|L-R|否|
|6|++|后缀自增|lexp++|rexp|L-R|否|
|7|- -|后缀自减|lexp- -|rexp|L-R|否|
|8|!|逻辑取反|!rexp|rexp|R-L|否|
|9|~|按位取反|~rexp|rexp|R-L|否|
|10|+|单目，表示正值|+rexp|rexp|R-L|否|
|11|-|单目，表示负值|-rexp|rexp|R-L|否|
|12|++|前缀自增|++rexp|rexp|R-L|否|
|13|- -|前缀自减|- -rexp|rexp|R-L|否|
|14|*|间接访问|*rexp|lexp|R-L|否|
|15|&|取地址|&lexp|rexp|R-L|否|
|16|sizeof|计算数据类型或变量占用的字节数|sizeof(rexp) 或 sizeof(类型)|rexp|R-L|否|
|17|（类型）|类型转换|(类型)rexp|rexp|R-L|否|
|18|*|乘法|rexp * rexp|rexp|L-R|否|
|19|/|除法|rexp / rexp|rexp|L-R|否|
|20|%|整数取余|rexp % rexp|rexp|L-R|否|
|21|+|加法|rexp + rexp|rexp|L-R|否|
|22|-|减法|rexp - rexp|rexp|L-R|否|
|23|<<|左移位|rexp << rexp|rexp|L-R|否|
|24|>>|右移位|rexp >> rexp|rexp|L-R|否|
|25|>|大于|rexp > rexp|rexp|L-R|否|
|26|>=|大于等于|rexp >= rexp|rexp|L-R|否|
|27|<=|小于等于|rexp <= rexp|rexp|L-R|否|
|28|==|等于|rexp == rexp|rexp|L-R|否|
|29|!=|不等于|rexp != rexp|rexp|L-R|否|
|30|&|按位与|rexp & rexp|rexp|L-R|否|
|31|^|按位异或|rexp ^ rexp|rexp|L-R|否|
|32|l|按位或|rexp l rexp|rexp|L-R|否|
|33|&&|逻辑与|rexp && rexp|rexp|L-R|是|
|34|ll|逻辑或|rexp ll rexp|rexp|L-R|是|
|35|?:|条件操作符|rexp ? rexp : rexp|rexp|N/A|是|
|36|=|赋值|lexp = rexp|rexp|R-L|否|
|37|+=|以...加|lexp += rexp|rexp|R-L|否|
|38|-=|以...减|lexp -= rexp|rexp|R-L|否|
|39|*=|以...乘|lexp *= rexp|rexp|R-L|否|
|40|/=|以...除|lexp /= rexp|rexp|R-L|否|
|41|%=|以...取模|lexp %= rexp|rexp|R-L|否|
|42|<<=|以...左移|lexp <<= rexp|rexp|R-L|否|
|43|>>=|以...右移|lexp >>= rexp|rexp|R-L|否|
|44|&=|以...与|lexp &= rexp|rexp|R-L|否|
|45|^=|以...异或|lexp ^= rexp|rexp|R-L|否|
|46|l=|以...或|lexp l= rexp|rexp|R-L|否|
|47|,|逗号|lexp, rexp|rexp|R-L|是|

#### 测试数据