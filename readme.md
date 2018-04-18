안드로이드에서는 중첩 인터페이스가 자주 사용된다. 그 개념이 부족하여 찾아 보던 중, 클래스와 인터페이스의 차이를 알고 싶어 정리한 내용이다.

## class
---
class는 객체를 생성하기 위한 필드(속성)와 메소드(동작)가 정의되어 있다. 여기서 객체는 class를 기반으로 구현할 대상이다. 추가적으로 그 대상을 실제로 구현한 실체를 인스턴스라고 하며 그 과정을 인스턴스화라고 한다.


비유하자면,
class : 자동차 설계도
객체 : 설계도 기반의 자동차 모형
인스턴스 : 모형에 맞는 실제의 자동차

![객체와 클래스의 관계](http://cfile6.uf.tistory.com/image/226A973B571BF6892CF299)




## interface
---
interface는 객체의 사용 방법을 정의한 타입이다. 이는 개발 코드와 객체가 서로 통신하는 접적 역할을 한다. 이는 사용 객체를 변경할 필요가 있을 때, 코드를 수정하지 않고, 새로운 객체만 interface에 대입하면 된다는 장점이 있다. 예를 들어 자동차의 바퀴를 한국 타이어에서 금호 타이어로 바꾸고 싶다면 아래와 같이 하면 된다.

```
Tire frontLeftTire = new HankookTire();
Tire frontLeftTire = new KumhoTire();

```



## 보충
---
이전에 이 내용을 공부하며 abstract class와 interface 개념이 헷갈렸던 기억이 난다. 추가적으로 그 차이를 되짚어 보자면,
* abstract class는 class이기 때문에 구현 할 때에 extends라는 표현을 쓰고, iterface는 implement를 사용한다.
* 이러이러한 메소드를 쓸 것이다.' 인터페이스에 선언을 해놓고, 가져다가 반드시 선언된 그대로 모두 구현하면 되는게 인터페이스이고, 이러이러한 메소드가 있지만 가져다 쓰거나 오버라이드 하거나, abstract가 붙은 메소드는 반드시 구현하면 되는게 abstract class이다.
