## 지그재그로 2차원 배열 채우기 해법3

```c
#include <stdio.h>
int main088() {
	int aList[5][5] = { 0 };
	int i = 0, j = 0, nCounter = 0, nOffset = 1;

	for (i = 0; i < 5; ++i) {
		//홀수 행과 짝수 행을 구별하고 첫 번쨰 요소의 초깃값을 결정한다.
		if (i % 2 == 0) nCounter = i * 5;
		else			nCounter = (i + 1) * 5 + 1;

		for (j = 0; j < 5; ++j) {
			//nOffset이 양수면 nCounter는 증가하고
			//음수면 반대로 감소한다.
			nCounter += nOffset;
			aList[i][j] = nCounter;
		}

		//토글 스위치처럼 행마다 양수/음수로 변경된다.
		//여기서 '-'는 부호 변경 연산자이다.
		nOffset = -nOffset;
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
>result

1       2       3       4       5 <br />
10      9       8       7       6 <br />
11      12      13      14      15 <br />
20      19      18      17      16 <br />
21      22      23      24      25 <br />