---
layout: post
title:  "abstract class"
date:   2022-06-05 00:00:00 +0200
description: Explain the class
---
추상클래스 
-----------------------------------------
추상 메소드란 자식 클래스에서 반드시 오버라이딩해야만 사용할 수 있는 메소드를 의미한다 추상 메소드를 선언하여 사용하는 목적은 추상 메소드가 포함된 클래스를 상속받는 자식 클래스가 반드시 추상 메소드를 구현하도록 하기 위해서이다 

- 선언
```
abstract 반환타입 메소드이름();
```
- 추상클래스 상속
부모클래스를 상속 받은 자식 클래스는 반드시 부모의 추상 함수를 구현해야 한다 부모클래스는 객체를 생성할 수 없기 때문에 자식 클래스에서 그 함수들을 구현 및 구체화해야한다 
```
class Dog extends Pet{
    public void walk(){
        System.out.println("Dog walk");
    }
    public void eat(){
    	System.out.println("Dog eat");
    }
}
```

-추상클래스의 특징
1.추상 클래스는 인스턴스, 즉 객체를 만들 수 없는 클래스이다
2.추상 메소드는 하위 클래스에서 메소드의 구현을 강제해야한다
3.추상 메소드를 포함하는 클래스는 반드시 추상 클래스여야한다
4.상속하는 집합간에는 연간관계가 있다
5.다중 상속이 불가능하다

-예제
```
abstract class Animal { 
    abstract void cry(); }

class Dog extends Animal { 
    void cry() { 
        System.out.println("멍멍!"); 
        } 
}

 public class Exam02 {

    public static void main(String[] args) {
        Animal a = new Animal();
        Dog d = new Dog();

        d.cry();
    }
}
```
