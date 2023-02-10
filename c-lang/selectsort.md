## 선택정렬

```c
#include <stdio.h>
int main0903() {
	int aList[5] = { 30, 40, 10, 50, 20 };
	int i = 0, j = 0, nMinIndex = 0, nTmp = 0;

	for (i = 0; i < 5; ++i) {
		nMinIndex = i;
		for (j = i + 1; j < 5; ++j) {
			if (aList[nMinIndex] > aList[j]) {
				nMinIndex = j;
			}
		}
		if (nMinIndex != i) {
			nTmp = aList[nMinIndex];
			aList[nMinIndex] = aList[i];
			aList[i] = nTmp;
		}
	}

	for (i = 0; i < 5; ++i) 
		printf("%d\t", aList[i]);
		
	putchar('\n');
	
	return 0;
}
```