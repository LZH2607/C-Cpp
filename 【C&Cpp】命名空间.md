# 【C&Cpp】命名空间



```c++
#include <iostream>

using namespace std;

int main() {
	cout << "Hello, World!" << endl;
	return 0;
}
```



```c++
#include <iostream>

using std::cout;
using std::endl;

int main() {
	cout << "Hello, World!" << endl;
	return 0;
}
```



```c++
#include <iostream>

int main() {
	using namespace std;
	cout << "Hello, World!" << endl;
	return 0;
}
```



```c++
#include <iostream>

int main() {
	using std::cout;
	using std::endl;
	cout << "Hello, World!" << endl;
	return 0;
}
```



```c++
#include <iostream>

int main() {
	std::cout << "Hello, World!" << std::endl;
	return 0;
}
```

