# 【C&Cpp】数据类型：double



double：64位



## 1.0 - 0.9 != 0.2 - 0.1

```c++
#include <iostream>

using namespace std;

int main() {
	double a = 1.0 - 0.9;
	double b = 0.2 - 0.1;
	if (a == b) {
		cout << "a == b" << endl;
	}
	else {
		cout << "a != b" << endl;
	}
	return 0;
}
```

