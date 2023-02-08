## 지그재그로 2차원 배열 채우기 해법 1
```c
#include <stdio.h>
int main0904() {
	int aList[5][5] = { 0 };
	int i = 0, j = 0, nCounter = 0;

	for (i = 0; i < 5; ++i) {
		if (i % 2 == 0) {
			for (j = 0; j < 5; ++j) {
				aList[i][j] = ++nCounter;
			}
		}
		else if (i % 2 != 0) {
			for (j = 4; j >= 0; --j) {
				aList[i][j] = ++nCounter;
			}
		}
	}

	for (i = 0; i < 5; ++i) {
		for (j = 0; j < 5; ++j) {
			printf("%d\t", aList[i][j]);
		}
		putchar('\n');
	}
	return 0;
}
```

> result

1       2       3       4       5 <br />
10      9       8       7       6 <br />
11      12      13      14      15 <br />
20      19      18      17      16 <br />
21      22      23      24      25 <br />