# About Java

## 들어가기
    처음 프로그래밍을 배울 때 자바로 시작하는 경우가 많다.
    자바를 설치하고, 환경 변수를 설정하고, 이클립스를 깔고, 따라 치고, 실행 하고..

    물론 처음에 자바가 무엇인지 부터 시작한다면 이해 할 수 없을 것이다. 
    그리고 배워왔던 것은 자바라는 언어가 어떤 특성을 갖는지 어떻게 사용하는지 등에 대해서이다.
    그러나 자바를 계속 사용하기 위해서는 언어외에도 계속 마주하는 용어들이나 작동하는 방식들에 
    대한 정리가 필요하다고 느꼈다.


## 플렛폼으로써의 자바
    자바(Java)는 자바로 기술된 프로그램 개발 및 실행을 할 수 있는 소프트웨어 모임의 총칭이다. 
    자바 프로그램은 운영체제나 하드웨어에 의존하지 않는 바이트 코드(중간 언어)인 추상적인 코드 로 구현된다. 
    따라서, 자바 프로그램을 실행하기 위해서는 자바 가상 머신(JVM)과 개발에 필요한 표준 라이브러리 세트와 컴파일러의 환경만 맞추면
    자바 프로그램은 모든 환경에서 동일하게 동작한다. 
    이러한 실행환경과 개발환경을 제공하는 것이 자바 플랫폼이다.

    자바 플랫폼은 자바 언어(Java Language), 자바 애플리케이션(Java Application), 자바 애플릿(Java Applet), JRE(Java Runtime Environment),
    자바 가상 머신(Java Virtual Machine), 모바일용 자바(Java ME), 자바 웹 스타트(Java Web Start) 등과 함께 단순히 「자바」(Java)라 불리는 경우가 많다.

    출처: https://ko.wikipedia.org/wiki/%EC%9E%90%EB%B0%94_(%EC%86%8C%ED%94%84%ED%8A%B8%EC%9B%A8%EC%96%B4_%ED%94%8C%EB%9E%AB%ED%8F%BC)


    내가 정리하고자 했던 내용을 직접 작성하는 것 보다 훨씬 뛰어나게 잘 요약된 글이 있어서 
    그대로 가져왔다.

    
    


## 자바의 실행방식 : 자바 플랫폼
    Java의 실행방식은 조금 특이하다.
    컴파일 언어와 인터프리터 언어의 방식을 모두 사용한다고 할 수 있다.

    먼저 개발자가 작성한 코드는 .java 파일에 저장이 된다.
    작성된 코드는 실행을 위해 컴파일이 되어야 하고 그 결과가 .class 파일이다.
    이 파일은 JVM(Java Virtual Machine)이라는 가상환경에서 실행된다. 
    이 때 실행되는 방식이 인터프리터 방식이다.
    JVM은 .class파일의 바이트 코드를 한줄 씩 해석하며 실행한다.

    WORA(Write Once, Read Anywhere)
    플랫폼에 종속되지 않고 사용하기 위해서 이 방식을 채택하였다는 것이 중요하다.
    
    컴파일이란 개발자가 작성한 코드를 실행 가능한 파일로 바꾸는 과정이라 생각하면 된다.
    그런데 CPU마다 명령어의 체계가 다르고 운영체제에 따라 API도 다르다. 
    따라서 일반적인 컴파일 언어에서 컴파일 된 파일은 다른 환경에서 작동하지 않을 가능성이 높다.
    
    Java의 경우 그것을 JVM을 통해 해결한다. 
    컴파일 된 바이트 코드는 JVM 위에서 실행되기에 환경에 신경쓰지 않고 실행될 수 있다.
    물론 컴파일 된 자파 파일 .class 파일을 해석할 수 있는 자바 플렛폼을 설치되어있어야만 하고, 
    특정 운영체제만 갖고있는 기능은 이용하지 못할 수도 있다는 단점이 있다.
    

## JDK, JRE
    다운로드를 하려다 보면 마주하게 되는 단어들이다.

    JRE은 Java Runtime Environment의 약자이다.
    JRE는 개발을 하지 않지만 자바 파일을 실행해야 하는 사람들이 다운 받으면 되는 것 이다.
    실행할 수 있도록 하는 JVM을 포함하여, 라이브러리 등이 포함된다.
    .class파일을 JVM에서 실행하기 위한 JIT(just in time) compiler,
    메모리의 관리를 도와주는 garbage collector등도 포함되어 있다.

    JDK는 Java Development Kit의 약자이며, 다시 말해 자바 개발을 하기 위해 필요한 묶음이다.
    코드를 작성하고 실행해볼 때는 라이브러리들도 필요하고, 컴파일의 과정도 거쳐야하며, 
    컴파일의 결과를 JVM위에서 실행도 해봐야 한다. 이런 모든 것들을 묶어서 배포하는 것이 JDK이다.
    따라서 JDK를 다운로드 받으면 JRE도 포함되어 있다.
    가장 중요한 차이는 컴파일을 하기 위한 javac의 포함 여부이며
    다른 javadoc(Java documentation generator)이나 jdb(Java Debugger)같은 툴또한 JDK에만 제공된다.
    
## JVM 추가 

    https://stackoverflow.com/questions/7674839/is-the-jvm-a-compiler-or-an-interpreter
    매우 좋은 글이 있어서 가져왔다. 직접 읽는 것이 더욱 좋다.
    
    질문 :
    JRE는 컴파일러냐 인터프리터냐 둘다 아니라면 무엇이냐?
    
    답 : 
    JVM is Java Virtual Machine -- Runs/ Interprets/ translates Bytecode into Native Machine Code
    JVM is a virtual platform that resides on your RAM
    Its component, Class loader loads the .class file into the RAM
    The Byte code Verifier component in JVM checks if there are any access restriction violations in your code. (This is one of the principle reasons why java is secure)
    Next, the Execution Engine component converts the Bytecode into executable machine code

    JVM은 램위에 존재하는 가상 플랫폼이다.
    그것의 구성요소인 Class loader는 .class파일을 램 위에 올린다.
    다른 구성요소인 Byte code Verifier는 코드의 접근 제한이나 위험을 검사한다.
    (이것이 자바가 안전한 이유 중 하나이다.)
    그리고 실행 엔진이 바이트 코드를 실행가능한 기계코드로 바꾼다.

    https://www.guru99.com/java-virtual-machine-jvm.html
    https://www.youtube.com/watch?v=G1ubVOl9IBw&t=2s
    이것 또한 참고할만하다.




## 버전 
    java version 을 보면 8, 9, 10, 11 이렇게 볼 수 도 있고
    1.7.2, 1.8.0과 같이 적혀있는 것도 볼 수 있다. 

    java 9 이전의 버전에서는 버전을 작성하는 방식이 달랐기 때문에, 1.8.0과 같이 작성되었다.
    9 이후의 버전에서는 java 9, java 11과 같이 작성한다.

    이전 버전에서 컴파일 된 파일은 이후 버전의 jre에서 실행이 가능하다.
    그러나 반대는 불가능하다.
    또한 이후 버전의 java에서 이전 버전으로 컴파일을 하는 것도 불가능하다.


    
 
## SE vs EE
    jdk를 다운로드 받을 때 선택하게 된다.
    SE는 Standard Edition, EE는 Enterprise Edition의 약자이다. 
    쉽게 말해 일반적으로 사용하기 위해서는 SE, 조금 더 많은 기능을 지원해주는 것이 EE이다.
    결합력을 낮추기 위한 DI, DB Transaction 처리, 로그 처리 등이 주요한 기능이였다. 
    
    EE는 유료인데다가 spring framework가 그 기능들을 잘 지원해 주기에
    요즘은 java se에 spring framework등을 얹어서 사용하는 경우도 많다.






## 참고
https://www.oracle.com/java/technologies/javase/jdk8-naming.html  
https://dzone.com/articles/a-guide-to-java-versions-and-features