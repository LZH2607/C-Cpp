# 【C&Cpp】static



[toc]



## 1. 面向过程

示例代码：

```c
#include <stdio.h>

void func(int a) {
	static int s; // 私有全局变量
	if (a == 0) {
		printf("%d\n", s);
	}
	else {
		s = a;
	}
}

int main() {
	func(0);
	func(1);
	func(0);

	return 0;
}
```

输出：

```
0
1
```



## 2. 面向对象

示例代码：

```c++
#include <iostream>

using namespace std;

class C {
public:
	int x;
	int y;
	static int s1; // 公有全局变量
private:
	static int s2; // 私有全局变量

public:
	void func(int a) {
		if (a == 0) {
			cout << s2 << endl;
		}
		else {
			s2 = a;
		}
	}
};

// 初始化
int C::s1 = 0;
int C::s2 = 0;

int main() {
	cout << sizeof(C) << endl;

	cout << C::s1 << endl;
	C::s1 = 1;
	cout << C::s1 << endl;
	
	C c;
	c.func(0);
	c.func(1);
	c.func(0);
	
	return 0;
}
```

输出：

```
8
0
1
0
1
```

