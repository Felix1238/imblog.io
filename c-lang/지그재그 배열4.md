## 지그재그로 2차원 배열 채우기 해법 4

```c
#include <stdio.h>
int main089() {
	int aList[5][5] = { 0 };
	//nFlag 변수는 반복문 내부에서 매번 참/거짓으로 바뀐다.
	int i = 0, j = 0, nCounter = 0, nFlag = 1;

	for (i = 0; i < 5; ++i) {
		//토글을 위한 플래그 변수
		if (nFlag) {
			//정방향 채우기
			for (j = 0; j < 5; ++j) {
				aList[i][j] = ++nCounter;
				//다음 반복에서 거짓인 경우가 선택되도록 한다.
			}
			nFlag = 0;
		}
		else {
			//역방향 채우기
			for (j = 0; j < 5; ++j) {
				aList[i][4 - j] = ++nCounter;
				//다음 반복에서 참인 경우가 선택되도록 한다.
			}
			nFlag = 1;
		}
	}
	
	//배열출력
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