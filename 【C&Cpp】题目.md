# 【C&Cpp】题目



[toc]



## 变量初始化

### Code 1

```c
#include <stdio.h>

struct {
	int a, b;
}t = { 1 };

int main() {
	printf("%d %d\n", t.a, t.b);
	printf("%d\n", t.a / t.b);
	return 0;
}
```

结果：

```
1 0
Exception: Integer division by zero
```



### Code 2

```c
#include <stdio.h>

void func() {
	int a;
	printf("%d\n", a);
}

int main() {
	func();
	return 0;
}
```

结果：

```
Error: 使用了未初始化的局部变量“a”
```



### Code 3

```c
#include <stdio.h>

void func() {
	static int a;
	printf("%d\n", a);
}

int main() {
	func();
	return 0;
}
```

结果：

```
0
```



### Code 4

```c
#include <stdio.h>

int a;

void func() {
	printf("%d\n", a);
}

int main() {
	func();
	return 0;
}
```

结果：

```
0
```



### Code 5

```c
#include <stdio.h>

void func() {
	static int i;
	++i;
	printf("%d\n", i);
}

int main() {
	func();
	return 0;
}
```

结果：

```
1
```



## 输出

### Code 1

```c
#include <stdio.h>

void func(char* p) {
	p = "abc";
}

int main() {
	char* p = "test";
	printf("%s\n", p);
	return 0;
}
```

结果：

```
test
```



## 变量大小

### Code 1

```c
#include <stdio.h>

struct stru {
	char c;
	int a;
};

union uni {
	char c;
	int a;
};

int main() {
	stru st = { 0 };
	uni un = { 0 };
	printf("%d\n", sizeof(st));
	printf("%d\n", sizeof(un));
	return 0;
}
```

结果：

```
8
4
```



### Code 2

```c
#include <stdio.h>

void func(int arr[2]){
	printf("%d\n", sizeof(arr));
}

int main() {
	int arr[2];
	printf("%d\n", sizeof(arr));
	func(arr);
	return 0;
}
```

结果：

```
8
8
```



### Code 3

```c
#include <stdio.h>

struct stru {
	char c;
	int a;
};

void func(stru arr[2]){
	printf("%d\n", sizeof(arr));
}

int main() {
	stru arr[2];
	printf("%d\n", sizeof(arr));
	func(arr);
	return 0;
}
```

结果：

```
16
8
```



### Code 4

```c
#include <stdio.h>
#pragma pack(8)

struct A {
	char c;
	double d;
	int i;
};

struct B {
	A a;
	int* ip;
	short int si;
};

int main() {
	printf("%d\n", sizeof(A));
	printf("%d\n", sizeof(B));
	return 0;
}
```

结果：

```
24
40
```



### Code 5

```c
#include <stdio.h>
#pragma pack(4)

struct A {
	char c;
	double d;
	int i;
};

struct B {
	A a;
	int* ip;
	short int si;
};

int main() {
	printf("%d\n", sizeof(A));
	printf("%d\n", sizeof(B));
	return 0;
}
```

结果：

```
16
28
```



### Code 6

```c
#include <stdio.h>

int main() {
	const char* str1 = "hello";
	char str2[] = "he";
	printf("%d\n", sizeof(str1));
	printf("%d\n", sizeof(str2));
	printf("%d\n", sizeof("hello"));
	return 0;
}
```

结果：

```
8
3
6
```

