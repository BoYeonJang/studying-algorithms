# [문자열 내 p와 y의 개수](https://school.programmers.co.kr/learn/courses/30/lessons/12916)

## 문제 설명
대문자와 소문자가 섞여있는 문자열 s가 주어집니다. s에 'p'의 개수와 'y'의 개수를 비교해 같으면 True, 다르면 False를 return 하는 solution를 완성하세요.<br>
'p', 'y' 모두 하나도 없는 경우는 항상 True를 리턴합니다.<br>
단, 개수를 비교할 때 대문자와 소문자는 구별하지 않습니다.<br>
<br>
예를 들어 s가 "pPoooyY"면 true를 return하고 "Pyy"라면 false를 return합니다.

## 제한사항
- 문자열 s의 길이 : 50 이하의 자연수
- 문자열 s는 알파벳으로만 이루어져 있습니다.

## 입출력 예
|s|answer|
|---|---|
|"pPoooyY"|true|
|"Pyy"|false|

## 입출력 예 설명
입출력 예 #1<br>
'p'의 개수 2개, 'y'의 개수 2개로 같으므로 true를 return 합니다.<br>
<br>
입출력 예 #2<br>
'p'의 개수 1개, 'y'의 개수 2개로 다르므로 false를 return 합니다.<br>
<br>
※ 공지 - 2021년 8월 23일 테스트케이스가 추가되었습니다.

## 문제
```python
def solution(s):
    answer = True
    
    # [실행] 버튼을 누르면 출력 값을 볼 수 있습니다.
    print('Hello Python')

    return True
```

## 풀이
```python
def solution(s):
    if s.lower().count('p') == s.lower().count('y'):
        return True
    else:
        return False
```

## 결과
||테스트 1|테스트 2|
|---|---|---|
|입력값|"pPoooyY"|"Pyy"|
|기댓값|true|false|
|실행 결과|테스트를 통과하였습니다.|테스트를 통과하였습니다.|

## 해설
- lower(): 대문자를 소문자로 바꿔주는 함수. WORLD → world<br>
- count(): 해당 문자열 안에서 찾고 싶은 문자의 개수를 찾게 해주는 함수. 'pPoooyY'.count('o') → 3<br>

따라서 s.lower().count('p')는 s안에 담긴 문자열을 소문자로 변환해주고 그 안에 담긴 p의 개수를 센다.<br>
s.lower().count('y')도 동일하게 소문자로 변환시킨 y의 개수를 세어서 둘을 비교한다.<br>
pPoooyY는 ppoooyy가 되어 p와 y가 각각 2개로 같으므로 True.<br>
Pyy는 pyy로 p가 1개, y가 2개로 개수가 다르므로 False.<br>
