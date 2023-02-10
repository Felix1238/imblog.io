## 파이썬 deque 정리
```python
from collections import deque
#기본적인 dque사용법
dq = deque('love')
#스택 구현
dq = deque('love')
dq.append('m') #오른쪽 끝에 항목 추가
deque(['l', 'o', 'v', 'e'])
dq.pop() #오른쪽 끝에 항목가져오면서 삭제
#큐 구현
dq = deque('love')
dq.appendleft('i') #완쪽에 i입력
dq.pop() #오른쪽에서 e출력
#depue 확장하기
dq = deque('love')
dq.extend('you') #오른쪽으로 you확장
dq.extendleft('i') #왼쪽으로 i확장
#리스트처럼 사용
dq = deque('love')
dq[2] = 'n' #인덱스를 이용한 항목 수정 v -> n
dq.insert(0, 'k') #첫번째 항목에 k 추가
dq.insert(100, 'k') #100번째 항목 (없으니까 가장 큰쪽에) k추가
dq.remove('k') #같은 항목이 있을때 왼쪽부터 지워짐햣
dq.remove('k') #오른쪽에 있는 k삭제
#deque의 내용을 좌우로 반전
dq = deque('love')
dq.reverse()
```
