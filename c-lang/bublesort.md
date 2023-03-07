## 버블정렬

666

```c
#include <stdio.h>
int main0902() {
	int aList[5] = { 30, 40, 50, 10, 20 };
	int i = 0, j = 0, nTmp = 0;

	for (i = 4; i >= 0; --i) {
		for (j = 0; j < i; ++j) {
			if (aList[j] > aList[j+1]) {
				nTmp = aList[j+1];
				aList[j+1] = aList[j];
				aList[j] = nTmp;
			}
		}
	}

	for (i = 0; i < 5; ++i)
		printf("%d\t", aList[i]);
	putchar('\n');

	return 0;
}
```