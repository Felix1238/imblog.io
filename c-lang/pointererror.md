## 중대한 2가지 오류

```c
#include <stdio.h>
#include <stdlib.h>

int main(void){
    char szBuffer[12] = {"HelloWorld"};
    char *pszData = NULL;

    pszData = (char*)malloc(sizeof(char) * 12);
    pszData = szBuffer;
    puts(pszData);
    return 0;
}
```

이코드에서 오류가 난 지점이 두개가 있다.

먼저 첫번째는 pszData = szBuffer; 이곳을 바르게 고치면
memcpy(pszData, szBuffer, sizeof(szBuffer));
이렇게 고쳐야되고

두번째는 할당된 메모리를 free()로 풀어주지 않았다는 것이다.