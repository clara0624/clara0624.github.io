---
layout: post
title:  "interface"
date:   2022-06-05 00:00:00 +0200
description: Explain the class
---
인터페이스
-------------------------------------------
인터페이스란 다른 클래스를 작성할 때 기본이 되는 틀을 제공하면서, 다른 클래스 사이의 중간 매개 역할까지 담당하는 클래스를 의미한다

-인터페이스 특징
1. 다중상속이 가능하다
    -> 자식 클래스가 여러 부모 인터페이스들을 상속받을 수 있다
2. 추상 메소드만 보유한다
    -> 인터페이스는 추상메소드만 가지고 있다
3. 생성자 생성이 불가하다
    ->디폴트생성자,인자 있는 생성자 모두 생성이 불가능하다
4. 메소드 오버라이딩 필수
    -> 자식클래스는 부모 인터페이스의 함수를 모두 오버라이딩 해야한다

-인터페이스를 사용하는 이유
인터페이스를 이용하여 클래스를 구현하면 다른 클래스와 대체가 유연해서 유지보수가 편해진다는 장점이 있기때문이다

-인터페이스 선언
인터페이스는 class가 아닌 interface 라는 키워드를 이용하여 작성한다
```
접근제어자 interface 인터페이스이름 {
    public static final 타입 상수이름 = 값;
    ...

    public abstract 메소드이름(변수목록);
    ...

}

```
인터페이스의 모든 필드는 public static final이어야 하며, 모든 메소드는 public abstract이어야 합니다

-인터페이스 구현
인터페이스는 자신이 직접 인스턴스를 생성할 수는 없다 따라서 인터페이스가 포함하고 있는 추상 메소드를 구현해 줄 클래스를 작성해야만 한다
```
class 클래스이름 implements 인터페이스이름 { ... }
```

-예제

```
interface Vehicle {
     public abstract void horn(); }

class Car implements Vehicle {
    public void horn() {
        System.out.println("경적소리!");
    }
}
public class Lecture01
    public static void main(String[] args) {
        Car c = new Car();
       
        c.horn();
        
```

-다중상속
인터페이스는 인터페이스로부터만 상속을 받을 수 있으며, 여러 인터페이스를 상속받을 수 있다

-예제

'''
package lecture20220821;

interface Vehicle {
    public abstract void horn(); }
interface transportation {
    public abstract void move(); }

class Car implements Vehicle, transportation {
    public void horn() {
        System.out.println("경적소리");

    }
    public void move() {
        System.out.println("이동 ");
    }
}

class Bicycle implements Vehicle, transportation {
    public void horn() {
        System.out.println("경적소리2");
    }
    public void move() {
        System.out.println("이동2");

    }

}

public class Lecture02 {
    public static void main(String[] args) {
        Car c = new Car();
        Bicycle b = new Bicycle();

        c.horn();
        c.move();
        b.horn();
        b.move();

    }
'''
위의 예제에서 car클래스와 Bicycle클래스는 각각 Vehicle와 Transportation클래스를 동시에 구현하고 있다
