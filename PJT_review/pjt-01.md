# 4Ls



## 좋았던 것(Liked)

- 그동안 단편적으로 사용하던 함수들을 총망라하여 사용할 수 있어 좋은 경험이었다.
- 동료들과 서로 모르는 것들은 질문하고 답변해주며 협업 능력을 기를 수 있었다.
- 내 손으로 짠 코드가 동작을 한다는 것이 신기하고도 즐거웠다.
- 앞으로 더 발전해서 더 좋은 코드를 만들 수 있겠다고 생각했다.



## 배운것(Learned)

- import json 명령어를 통해 외부 파일들을 불러오는 방법에 대해 알게 되었다.
  - json(JavaScript Object Notation)
    - XML, YAML과 함께 효율적으로 데이터를 저장하고 교환하는데 사용하는 텍스트 데이터 포맷
    - 읽고 쓰기 쉬움
    - C-family 프로그래밍 언어의 규약을 따름

```python
import json

file_addr = open('user/file.txt')
file = json.load(file_addr)
```

- pprint(Pretty Print)
  - 문자 그대로 출력을 아름답게 출력해주는 명령어
  - 5가지 옵션 조정이 가능하다.
    - depth (중첩된 데이터의 출력 수준)
    - indent (들여쓰기)
    - width (줄 길이 제한)
    - sort_dicts (딕셔너리 키 정렬)
    - stream (파일에 스트림 출력)

```python
from pprint import pprint
pprint(result)
```



## 부족했던 것(Lacked)

- 함수를 정의하는 것에 아직 익숙하지 않다.
- for 문을 활용하여 반복되는 구조를 아직 완전히 이해하지 못했다.
- 변수를 선언하는 위치에 대한 이해가 더 필요하다.
  - 변수의 indent에 따라 변수가 계속 반복될 수도 있음에 유의하자.
  - 변수가 계속 새로이 갱신되어 무한 반복 되는 것 같은 현상이 발생했다.
- for 문을 중첩하여 사용할 때 그 메커니즘에 대한 이해가 더 필요하다.

```python
for pocket in pockets:	
    for items in pocket:
    	for item in items:
            
'''
for 문 중첩이 필요한 경우와 어떻게 중첩을 사용해야 할지 신중히 생각해보자.
꼭 이전의 변수가 나올 필요는 없다..
''' 
```

- 출력을 리스트로 하는 것도 잘 모르고 있었다. 
  - 기본적인 것에 대한 추가적인 공부가 필요하다

```python
a = []
a.append(items)
print(a)
'''
같읕 구문들에 조금 더 익숙해지도록 하자
'''
```



## 바라는 것(Longed for)

- 더 다양한 관통 프로젝트를 경험해 보고 싶다.
- 내게 부족한 점들을 더 공부하여 다음 번 프로젝트 때는 더 나아진 코드를 짜보고 싶다.