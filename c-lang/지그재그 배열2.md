## 지그재그로 2차원 배열 채우기 해법 2

```c
#include <stdio.h>
int main087() {
	int aList[5][5] = { 0 };
	int i = 0, j = 0, nCounter = 0;

	for (i = 0; i < 5; ++i) {
		//짝수 행과 홀수 행을 구별한다.
		if (i % 2 == 0)
			//짝수행
			for (j = 0; j < 5; ++j)
				//순방향으로 행을 채운다
				aList[i][j] = ++nCounter;
		else
			//홀수행
			for (j = 0; j < 5; ++j)
				aList[i][4 - j] == ++nCounter;
	}
	//배열 출력
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