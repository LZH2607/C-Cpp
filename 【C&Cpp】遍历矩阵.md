# 【C&Cpp】遍历矩阵



[toc]



代码：

```c++
#include <iostream>

using namespace std;

int main() {
	char a[5][5] = {
		{'a','b','c','d','e'},
		{'f','g','h','i','j'},
		{'k','l','m','n','o'},
		{'p','q','r','s','t'},
		{'u','v','w','x','y'}
	};

	for (int i = 0; i < 5; i++) {
		for (int j = 0; j < 5; j++) {
			cout << a[i][j] << " ";
		}
		cout << endl;
	}
	return 0;
}
```

输出：

```
a b c d e
f g h i j
k l m n o
p q r s t
u v w x y
```



代码：

```c++
#include <iostream>

using namespace std;

int main() {
	char a[5][5] = {
		{'a','b','c','d','e'},
		{'f','g','h','i','j'},
		{'k','l','m','n','o'},
		{'p','q','r','s','t'},
		{'u','v','w','x','y'}
	};

	for (int j = 0; j < 5; j++) {
		for (int i = 0; i < 5; i++) {
			cout << a[i][j] << " ";
		}
		cout << endl;
	}
	return 0;
}
```

输出：

```
a f k p u
b g l q v
c h m r w
d i n s x
e j o t y
```



代码：

```C++
#include <iostream>

using namespace std;

int main() {
	char a[5][5] = {
		{'a','b','c','d','e'},
		{'f','g','h','i','j'},
		{'k','l','m','n','o'},
		{'p','q','r','s','t'},
		{'u','v','w','x','y'}
	};

	for (int i = 0; i < 5; i++) {
		for (int j = 0; j <= i; j++) {
			cout << a[i][j] << " ";
		}
		cout << endl;
	}
	return 0;
}
```

输出：

```
a
f g
k l m
p q r s
u v w x y
```



代码：

```c++
#include <iostream>

using namespace std;

int main() {
	char a[5][5] = {
		{'a','b','c','d','e'},
		{'f','g','h','i','j'},
		{'k','l','m','n','o'},
		{'p','q','r','s','t'},
		{'u','v','w','x','y'}
	};

	for (int i = 0; i < 5; i++) {
		for (int j = 0; j < 5 - i; j++) {
			cout << a[i][j] << " ";
		}
		cout << endl;
	}
	return 0;
}
```

输出：

```
a b c d e
f g h i
k l m
p q
u
```



代码：

```c++
#include <iostream>

using namespace std;

int main() {
	char a[5][5] = {
		{'a','b','c','d','e'},
		{'f','g','h','i','j'},
		{'k','l','m','n','o'},
		{'p','q','r','s','t'},
		{'u','v','w','x','y'}
	};

	for (int i = 0; i < 5; i++) {
		for (int j = 0; j < i; j++) {
			cout << "  ";
		}
		for (int j = i; j < 5; j++) {
			cout << a[i][j] << " ";
		}
		cout << endl;
	}
	return 0;
}
```

输出：

```
a b c d e
  g h i j
    m n o
      s t
        y
```



代码：

```c++
#include <iostream>

using namespace std;

int main() {
	char a[5][5] = {
		{'a','b','c','d','e'},
		{'f','g','h','i','j'},
		{'k','l','m','n','o'},
		{'p','q','r','s','t'},
		{'u','v','w','x','y'}
	};

	for (int i = 0; i < 5; i++) {
		for (int j = 0; j < 5 - i - 1; j++) {
			cout << "  ";
		}
		for (int j = 5 - i - 1; j < 5; j++) {
			cout << a[i][j] << " ";
		}
		cout << endl;
	}
	return 0;
}
```

输出：

```
        e
      i j
    m n o
  q r s t
u v w x y
```

