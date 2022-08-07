# 목표

- Python 기본 문법 습득
- 데이터 구조에 대한 분석과 이해
- 요청과 응답에 대한 이해
- API 활용과 API 문서 숙지



# 4Ls

## 좋았던 것(Liked)

- 지난 주보다는 수월하게 프로젝트를 진행할 수 있어 발전했다는 생각이 들었다.
- 새로 배운 try, except 구문을 사용해 볼 수 있어 좋았다.
- 외부 api를 사용해볼 수 있는 좋은 경험이었다.



## 배운것(Learned)

- sort 함수의 lambda 파라미터에 대해 새롭게 배우게 되었다.

```python
# 리스트 내 딕셔너리 정렬
list = [
    {'name' : 'a', 'age' : 11},
    {'name' : 'b', 'age' : 4},
    {'name' : 'c', 'age' : 6},
    {'name' : 'd', 'age' : 2}
]

a = sorted(list, key = lambda x : x['age'], reverse=True/False)
print(a)
# [
{'name' : 'd', 'age' : 2}
{'name' : 'b', 'age' : 4}
{'name' : 'c', 'age' : 6}
{'name' : 'a', 'age' : 11}
]
```

- requests

```python
import requests

URL = 'https://www.example.com/'

param = {
    'key1' : 'value1',
    'key2' : 'value2'
}

exam = requests.get(URL, params = param).json() 
# https://www.example/?key1=value1&key2=value2

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

- 새로운 것을 도입하고자 할 때 개념 적응에 시간이 꽤 소요된다.
- 예제를 적극적으로 활용하지 못했다.
- 예외 처리에 있어 if 구문이 복잡해지는 것을 피하고자 try, except 문을 사용했는데, 시간을 투자해서 적용해보았으면 좋겠다.



## 바라는 것(Longed for)

- 더 다양한 관통 프로젝트를 경험해 보고 싶다.
- 내게 부족한 점들을 더 공부하여 다음 번 프로젝트 때는 더 나아진 코드를 짜보고 싶다.