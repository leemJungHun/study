Hilt
===============
Hilt란?
--------------
> - Dagger 기반의 DI 라이브러리
> - Annotation을 이용한 컴파일 타임 generated code로 의존성 주입을 구현
> - 기존 Dagger보다 **보일러 플레이트 코드**가 줄어들었으며 진입장벽이 낮음
>    - **보일러 플레이트 코드**는 최소한의 변경으로 여러곳에서 재사용되며, 반복적으로 비슷한 형태를 띄는 코드를 말한다.

[DI]의존성 주입이란?
--------------
> - DI(Dependency Injection)
> - 외부에서 의존 객체를 생성하여 넘겨주는 것(ex: A클래스가 B클래스를 의존할 때 B Object를 직접 생성하지 않고 외부에서 생성해서 넘겨주는 것)
> 
> <img src="https://taehyungk.github.io/img/DI_inject.jpeg" width="450px" height="300px"></img><br/>

DI는 왜 필요한가?
--------------------
> - 의존성 파라미터를 생성자에 작성하지 않아도 되므로 보일러 플레이트 코드를 줄일 수 있다.
> - Interface에 구현체를 쉽게 교체하면서 상황에 따라 적절한 행동을 정의할 수 있다. 특히 테스팅 시에 Mock 객체(모의 객체)와 실제 객체를 바꿔가며 테스트할때 용이하다.
> - 의존 받는 객체는 의존 객체의 구현을 알 필요가 없다.

Dagger 기본 개념
-------------------------
### Dagger에는 아래와 같이 5가지의 필수 개념이 있다
> - Inject
> - Component
> - Subcomponent
> - Module
> - Scope

### Inject
> - 의존성 주입을 요청
> - Inject 어노테이션으로 주입을 요청하면 연결된 Component가 Module로 부터 객체를 생성해서 넘겨줌

### Component
