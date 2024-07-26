https://covenant.tistory.com/224



``` python
###### 문제 설명

정수 `n`이 매개변수로 주어질 때, `n`의 약수를 오름차순으로 담은 배열을 return하도록 solution 함수를 완성해주세요.

---

##### 제한사항

- 1 ≤ `n` ≤ 10,000

---

##### 입출력 예

|n|result|
|---|---|
|24|[1, 2, 3, 4, 6, 8, 12, 24]|
|29|[1, 29]|
```



``` python
def solution(n):
    
    answer = []
    for i in range(1, n+1):
        if n % i == 0:
            answer.append(i)
    return answer

```


``` python
###### 문제 설명

이진수를 의미하는 두 개의 문자열 `bin1`과 `bin2`가 매개변수로 주어질 때, 두 이진수의 합을 return하도록 solution 함수를 완성해주세요.

---

##### 제한사항

- return 값은 이진수를 의미하는 문자열입니다.
- 1 ≤ `bin1`, `bin2`의 길이 ≤ 10
- `bin1`과 `bin2`는 0과 1로만 이루어져 있습니다.
- `bin1`과 `bin2`는 "0"을 제외하고 0으로 시작하지 않습니다.

---

##### 입출력 예

|bin1|bin2|result|
|---|---|---|
|"10"|"11"|"101"|
|"1001"|"1111"|"11000"|
```


```
def solution(bin1, bin2):
    num1 = int(bin1, 2)
    num2 = int(bin2, 2)
    
    # 두 수를 더함
    sum_num = num1 + num2
    answer = bin(sum_num)[2:]
    print(answer)

    return answer
```