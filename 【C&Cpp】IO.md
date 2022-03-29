# 【C/C++】I/O



[toc]



## C语言：输入一行（无空格）

```c
#include <stdio.h>

int main() {
	char c[100];
	scanf("%s", c);
	printf("%s", c); 
	return 0;
}
```



## C语言：输入一行（有空格）

```c
#include <stdio.h>

int main() {
	char c[100];
	scanf("%[^\n]", c);
	printf("%s", c);
	return 0;
}
```

```c
#include <stdio.h>

int main() {
	char c[100];
	gets(c);
	printf("%s", c); 
	return 0;
}
```



## C++：输入一行（无空格）

```c++
#include <iostream>

using namespace std;

int main() {
	string s;
	cin >> s;
	cout << s << endl;
	return 0;
}
```



## C++：输入一行（有空格）

```c++
#include <iostream>
#include <string>

using namespace std;

int main() {
	string s;
	getline(cin, s);
	cout << s << endl;
	return 0;
}
```

```c++
#include <iostream>

using namespace std;

int main() {
	char c[100];
	cin.getline(c, 100);
	cout << c << endl;
	return 0;
}
```

