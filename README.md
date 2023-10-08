### 배열
push, pop은 O(1)
shift, unshift은 O(n)

알고리즘 해결방법
1. 문제 해결을 위한 계획 수립
2. 일반적인 문제 해결 패턴을 파악


계획 수립 - 방향이나 기본적 개념을 알고 있다는 것을 보여줄 수 있다

리팩토링 질문
can you check the result?

can you derive the result differently?
문제에 대한 해결책이 하나만 있는 경우는 드물기 때문에 이런 질문이 가능
can you understand it at a glance?
can you use the result or method for some other problem?
can you improve the performance of your solution?
can you think of other ways to refactor?
how habe other people solved this problem?


루프는 중첩 루프보다 개별 루프가 훨씬 효율적 ex: 개별루프 2개와 이중루프의 경우, 1000개의 작업을 수행하게 되면 2000 vs 10^6


슬라이드 윈도우
배열에서 n개의 연속된 수의 합을 구하는 경우
매번 루프를 도는 대신, 첫째값과 마지막값만 참조함

### 선형 탐색
배열은 정렬되어 있어야 함 O(n)

### 이진 탐색
배열은 정렬되어 있어야 함
배열을 둘로 나누고, 위아래로 탐색 O(logn)


### 재귀

- 중단점이 필요

- 중단점 > 실행코드 > 재귀호출

- 종료 조건이 없으면 스택에 계속해서 함수를 추가하게 됨
> 스택이 넘침

- 잘못된 값을 반환하거나, 애초에 반환하지 않는 것
>   종료 조건을 제대로 설정했지만, 위와 같은 경우에 종료 조건에 도달하지 못함
ex : 재귀 호출을 하는 과정에서 값을 감소시켜야 하는데, 이에 대한 로직이 빠진 경우

### 헬퍼 매소드 재귀
일종의 결과를 컴파일할 때 흔히 사용되는 패턴으로, 결과는 보통 배열이나 배열과 비슷한 다른 형태 데이터 구조이다.

- 재귀 호출을 하는 과정에서 배열 등의 자료 구조나 변수 등이 초기화되는 문제를 해결해줌

- 재귀적이지 않은 함수가 재귀적인 내부 함수를 호출하는 패턴

- 배열을 사용하고 헬퍼 메소드 없이 순수 재귀 솔루션을 작성하는 경우, 배열을 복사하는 slice, spread 연산자(operator), concat 같은 메서드를 사용해 배열을 변경하지 않을 수 있다.

