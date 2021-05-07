# iterable 객체(ierable과 iterator)
    쉽게 이해하고 싶은 사람은 iterable한 타입이란 
    iterator라는 어떤 객체를 통해 다음 값에 접근 할 수 있도록 설계되어 진 것이라 생각하면 된다.
    대표적으로 list, tuple, dictionary, set, range, string이 있고
    그리고 iterable한 객체들은 for문에서 사용될 수 있다는 것까지 알아두면 좋다.

    

    iterator = 반복자, iterable = 반복가능한 타입이라고 생각을하면 쉽다. 
    
    예시를 작성해보겠다.
    list 와 list에 대한 iterator는 다음과 같이 생성할 수 있다.
    
    a = [1, 2, 3, 4, 5]
    a_iterator = iter(a)
    next(a_iterator)

    a 는 list고 이는 iterable한 타입이다.
    그리고 다음줄에 선언한 a_iterator가 리스트 a에 대한 iterator이다. 
    리스트 a에 대한 iterator가 생성가능하므로 a는 iterable하다고도 할 수 있다. 
    a_iterator는 next라는 함수를 통해 리스트의 다음 값에 접근 할 수 있다. 
    이렇듯 iter()을 이용하여 iterator 객체를 생성가능한 것들을 iterable 하며
    iterable 한 객체는 내부적으로 매직메소드 __iter__를 갖고 있다.


    디자인 패턴에서 iterator 패턴이 있다.
    정의는 '컬렉션 구현 방법을 노출시키지 않으면서도 그 집합체안에 들어있는 
    모든 항목에 접근할 수 있게 해 주는 방법을 제공해 주는 패턴' 이다.

    실제로 대부분은 for문에서 iterable한 객체가 쓰일 수 있다는 것은
    아는 반면 이게 어떻게 가능한 것인지는 모른다. 
    그것 자체로 컬렉션의 구현 방법을 노출시키지 않았다고 할 수 있다.
    또한 위의 예제에서도 iterator 객체를 통해 원하는 값에 접근은 가능한 반면
    실제로 list라는 컬렉션이 어떻게 구현되어 있는지에 대한 정보를 알 필요가 없다.


    참고)
    https://suwoni-codelab.com/python%20%EA%B8%B0%EB%B3%B8/2018/03/06/Python-Basic-Iterable-iterator/


# for in문에서 iterable 객체
    파이썬에서는 주로 for in 문을 사용하여 반복문을 나타낸다. 
    for in 문에서 반복의 조건으로 iterable 객체들이 사용될 수 있다.
    iterable 객체란 반복이 가능한 객체로 list, tuple, dictionary, set, range, string, byte들이 이에 해당한다.

    사용방법은 다음과 같다.
    for item in iterable:
        반복할 부분....
    ex)
    for i in range(20):
        print(i)

    다른 언어에서는 주로 몇번째 반복인지의 count를 이용해서 list[count]처럼 접근해야 했던 것과는 달리, 바로 그 시행에서의 item을 이용할 수 있다.


# iterable한 객체를 list로

    list() 함수를 이용하여 iterable한 타입의 객체를 list로 바꿀 수 있다.

    a = list(range(10))
    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    
    b = list(combinations([1, 2, 3, 4], 2))
    [(1, 2), (1, 3), (1, 4), (2, 3), (2, 4), (3, 4)]

