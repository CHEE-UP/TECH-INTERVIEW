## Python

1. ##### 파이썬 제너레이터에 대해 설명해주세요

   > 제너레이터는 for 문을 돌렸을때 한번에 반환되는 값과달리, 값 하나만 반환하고 대기상태에 걸리는 반복자입니다. 원하는 시점에 데이터를 얻기에 좋습니다. next() 메서드를 호출하여 값을 반환하고 자원을 해제하기 때문에 메모리 낭비가 적습니다. list.append() 하는것보다 훨씬 효율이 좋음 

2. ##### list 와 튜플의 차이가 뭔가요?

   > tuple () , list 는 []으로 생성을 합니다. tuple 은 변경 불가능(immutable)하고, list 는 변경 가능(mutable) 합니다.

3. ##### 파이썬의 메모리관리

   > 파이썬은 모든것이 객체로, heap 에서 메모리 관리를 하게 됩니다. 파이썬 인터프리터에서만 접근 가능하며, 프로그래머가 관리하지 않습니다. 

4. ##### lambda 가 뭔가요?

   > 이름을 정의하지않는 함수입니다. 보통 한 줄로 간단하게 만들 때 사용합니다. 한번 쓰이고 다음 라인으로 넘어갈때 메모리 공간에서 제거되는 장점이있다. 

5. ##### docstring이란 무엇인가요?

   > 모듈, 함수, 클래스 앞에 선언되는 주석입니다. 안 써봤지만, 찾아본 결과 코드 실행중에도 소스 코드에 첨부한 문서에 직접 접근할 수 있습니다.

6. ##### *Args 와 *kwargs 차이 

   > N개의 매개변수를 넘깁니다.
   >
   > example
   >
   > ```python
   > def sample(*Args):
   >     for arg in Args:
   >         print(arg)
   > sample('hello','world','test','simple')
   > ```
   >
   > ##### *KwArgs 란?
   >
   > N개의 매개변수를 넘길 때 , key 와 value 값이 둘다 넘깁니다.
   >
   > ```python
   > def sample(**Kwargs):
   >     for i,v in Kwargs:
   >         print(i,v)
   > sample(hello='hello',second='world',hoho='test',haha='simple')
   > ```

7. ##### python 에 Main() 메서드가 있나요?

   > 인터프리터 언어라 code by code 로 실행합니다. magic method 가 있어서 `__main__` 실행된 모듈 이름이 저장되는데, 그 값이 name 값과 동일할 경우 조건문 안의 값에 메인 함수를 만들어 호출 할 수 있습니다.

8. ##### iterable 과 iterator 의 의미와 차이를 알려주세요

   > __iteratable__ 은 멤버를 하나씩 차례로 반환 __가능한__ 객체입니다. list , str , tuple, dict 이 대표적으로 있다. `__iter()__` 나 `__getitem__` 으로 정의된 클래스는 모두 iterable 합니다.
   >
   > __iterator__ 는 한번에 하나의 값을 반환하는 객체입니다. _next()_ 메서드를 통해 데이터를 순차적으로 호출 가능한 객체. bool 값을 반환하며, 다음 데이터가 없을 경우 예외가 발생합니다.
   >
   > list 의 경우, 이터러블 한 객체이나 next() 쓰면 에러가 납니다. 왜냐면 list return 시 모든 값을 반환하기 때문에, iter() 함수로 _**listiterator**_ 로 반환 후 next()함수를 쓰면 하나씩 반환하여 사용할 수 있습니다.

9. ##### 클래스 메서드의 self 뜻

   > 클래스의 객체를 의미합니다. 객체가 생성될 경우, 해당 객체는 self 로 들어갑니다.

