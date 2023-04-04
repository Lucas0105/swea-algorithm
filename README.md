## Why 왜 알고리즘을 공부하는가?
알고리즘 문제를 해결하는 것이 재밌어서 시작하였습니다.

## 목표
1일 1알고리즘을 수행하자

## 배운 내용


### 모듈러 연산
어떠한 숫자를 다른 숫자로 나눈 나머지를 구하는 연산    
- 성질 1
```
(a + b) mode m = ((a mod m) + (b mod m)) mod m
```

- 성질 2
```
(a * b) mode m = ((a mod m) * (b mod m)) mod m
```

- 증명 1
```
a mod m = T       
b mod m = S       

a = T + i*m (i는 임의의 정수)          
b = S + j*m (j는 임의의 정수)   

(a + b) mode m = ((a mod m) + (b mod m)) mod m

(T + i*m + S + j*m) mod m = (T + S + (i + j)m) mod m = (T + S) mod m

(T + S) mod m = ((a mod m) + (b mod m)) mod m
```
(i + j)m 을 m으로 나눈 나머지 값은 0이기 때문에 제거해주었습니다.

- 증명 2         
위의 증명 1과 동일한 방식으로 수행하면 성립합니다.

```
(a * b) mode m = ((a mod m) * (b mod m)) mod m
```


### 이항계수
n개의 원소에서 k개의 원소를 뽑아내는 경우의 수 (nCr)

- 성질
```
nCr = n-1Cr + n-1Cr-1
```

- 풀이
```
n개의 원소 중 r개를 선택하는 경우의 수는 

n-1개의 원소 중 r개를 선택하는 경우의 수 +

n-1개의 원소 중 r-1개의 원소를 선택하는 경우의 수와 일치

그 이유는 n개의 원소를 다룰 수 있는 방법이 2가지밖에 없기 때문입니다.
n개의 원소 중 하나의 원소를 뽑거나 하나의 원소를 뽑지 않는 경우밖에 없습니다.

n개의 원소 중 하나의 원소를 뽑는 경우 = n-1Cr-1
하나의 원소를 뽑지 않는 경우 = n-1Cr
```

- 팩토리얼로 문제를 해결하지 않는 이유

팩토리얼은 값이 커질 수록 실행하는 연산의 수가 급격히 커지기 때문입니다.

- 시간복잡도
O(nk)

### 관련 문제
- https://www.acmicpc.net/problem/11051


### 최장 증가 부분 수열(LIS) 알고리즘
Longest Increasing Subsequence     
```
어떤 임의의 수열이 주어질 때, 이 수열에서 몇 개의 수들을 제거해서 부분수열을 만들 수 있다. 
이때 만들어진 부분수열 중 오름차순으로 정렬된 가장 긴 수열을 최장 증가 부분 수열이라 한다.
```

- 풀이(동적계획법)
```
i를 현재 위치로 생각하고 j를 이전 배열들의 위치라고 생각합니다. (j < i)

현재의 값보다 j의 값이 작으면 수열이 가능하기 때문에 j의 위치에 + 1을 하여 수열의 길이를 dp에 저장해줍니다.

해당 값들 중에 가장 큰 값을 저장하면 LIS가 됩니다.

for문을 두번 돌려야 하기 때문에 O(n2)의 시간이 걸립니다.

```


## 시작 기간
2023-02-20 ~ 


## 결과
