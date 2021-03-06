# 3 코드에서 나는 악취

## 3.1 기이한 이름Mysterious Name

코드를 명료하게 표헌하는 데 가장 중요한 요소 하나는 바로 '이름'이다. 이름 바꾸기는 단순히 이름을 다르게 표현하는 연습이 아니다. 마땅한 이름이 떠오르지 않는다면 설계에서 더 근본적인 문제가 숨어있을 가능성이 높다. 그래서 혼란스러운 이름을 잘 정리하다 보면 코드가 훨씬 간결해질 때 가 많다.

## 3.2 중복Duplicated Code

## 3.3 Long function

주석을 달아야 할 만한 부분은 무조건 함수로 만든다. 그 함수 본문에는 원래 주석으로 설명하려던 코드가 담기고, 함수 이름은 동작 방식이 아닌 <strong>의도intention</strong>가 드러나게 짓는다. 이렇게 함수로 묶는 코드는 여러 줄일 수 도 있고 단 한줄일 수도 있다. 심지어 원래 코드보다 길어지더라도 함수로 뽑는다. 단 함수 이름에 코드의 목적이 들어나야 한다. 여기서 핵심은 함수의 길이가 아닌, 함수의 목적(의도)과 구현 코드의 괴리가 얼마나 큰가이다. 즉 '무엇을 하는지'코드가 잘 설명해주지 못할수록 함수로 만드는게 유리하다.

함수를 짧게 만드는 작업의 99%는 **함수 추출하기**가 차지한다. 함수 본문에서 따로 묶어 뺴내면 좋은 코드 덩어리를 찾아 새로운 함수로 만드는것이다.

함수가 매개변수와 임시변수를 많이 사용한다면 추출작업에 방해가 된다. 이런 상황에서 함수를 추출하다 보면 추출된 함수에서도 매개변수가 너무 많아져서 리팩터링 전보다 난해해질 수 있다. 그렇다면 **임시 변수를 질의 함수로 바꾸기**로 임시 변수의 수를, **매개변수 객체 만들기**와 **객체 통째로 넘기기**로 매개변수의 수를 줄일 수 있을 것이다.

이 리팩터링들을 적용해도 여전히 임시 변수와 매개변수가 너무 많다면 더 큰 수술이라 할 수 있는 **함수를 명령으로 바꾸기**를 고려해보자.

반복문도 그 안의 코드와 함께 추출해서 독립된 함수로 만든다. 추출한 반복문 코드에 적합한 이름이 떠오르지 않는다면 성격이 다른 두가지 작업이 섞여 있기 때문일 수 있다. 이럴 때는 과감히 **반복문 쪼개기**를 적용해서 작업을 분리한다.

## 3.4 Long Parameter List

## 3.5 Global Data

## 3.6 Mutable Data

## 3.7 뒤엉킨 변경Divergent Change

### 3.8 산탄총 수술

### 3.9 기능 편애

함께 변경할 대상들을 한데로 모으자

### 3.10 데이터 뭉치

### 3.11 기본형 집착Primitive Obsession

금액,물리량, 전화번호등 기본형으로 표현되어 있는 자료가 있다면 **기본형을 객체로 바꾸기**를 적용해보자.

### 3.12 반복되는 Switch문

### 3.13 반복문

**반복문을 파이프라인으로 바꾸기**를 적용한다.

### 3.14 성의 없는 요소Lazy Element

본문 코드를 그대로 쓰는 것과 진배없는 함수도 있고, 실질적으로 메서드가 하나뿐인 클래스도 있다.

이런 프로그램 요소는 고이 보내드리는게 좋다.

### 3.15 추측성 일반화Speculative Generality

이 냄새는 '나중에 필요할 거야'라는 생각으로 당장은 필요 없는 모든 종류의 후킹 포인트와 특이 케이스 처리 로직을 작성해둔 코드에서 풍긴다.

### 3.16 임시 필드

### 3.17 메시지 체인

메서드 체인이 너무 길어지고, 해당 요소가 반복적으로 불러와진다면 해당 요소를 호출하는 메서드를 따로 만들어보자.

### 3.18 중개자

### 3.19 내부자 거래

### 3.20 거대한 클래스

### 3.21 서로 다른 인터페이스의 대안 클래스들

### 3.22 데이터 클래스

### 3.23 상속 포기

### 3.24 주석

주석을 달면 안된다고 말하려는 건 아니니 걱정하지 말자. 주석은 악취가 아닌 향기를 입힌다. **문제는 주석을 탈취체 처럼 사용하는 데 있다.** 주석이 장황하게 달린 원인이 코드를 잘못 작성 했기 때문인 경우가 의외로 많다. **주석을 남겨야겠다는 생각이 들면, 가장 먼저 주석이 필요 없는 코드로 리팩터링을 해본다.**






