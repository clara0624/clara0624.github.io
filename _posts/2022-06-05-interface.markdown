---
layout: post
title:  "interface"
date:   2022-06-05 00:00:00 +0200
description: Explain the class
---
인터페이스
-------------------------------------------
인터페이스란 다른 클래스를 작성할 때 기본이 되는 틀을 제공하면서, 다른 클래스 사이의 중간 매개 역할까지 담당하는 일종의 추상 클래스를 의미한다

-인터페이스 특징
1. 다중상속이 가능하다
    -> 자식 클래스가 여러 부모 인터페이스들을 상속받을 수 있다
2. 추상 메소드만 보유한다
    -> 인터페이스는 추상메소드만 가지고 있다
3. 생성자 생성이 불가하다
    ->디폴트생성자,인자 있는 생성자 모두 생성이 불가능하다
4. 메소드 오버라이딩 필수
    -> 자식클래스는 부모 인터페이스의 함수를 모두 오버라이딩 해야한다

-인터페이스 선언
인터페이스는 class가 아닌 interface 라는 키워드를 이용하여 작성한다
<pre>
<code>
interface Animal {
}

class Human {
    String name;

    void setName(String name) {
        this.name = name;
    }
}</code>
</pre>
-인터페이스 구현
인터페이스는 자신이 직접 인스턴스를 생성할 수는 없다 따라서 인터페이스가 포함하고 있는 추상 메소드를 구현해 줄 클래스를 작성해야만 한다
<pre>
<code>
class 클래스이름 implements 인터페이스이름 { ... }</code>
</pre>

-인터페이스를 사용하는 이유
인터페이스를 이용하여 클래스를 구현하면 다른 클래스와 대체가 유연해서 유지보수가 편해진다는 장점이 있기때문이다

-예제
<pre>
<code>
interface Animal {
     public abstract void cry(); }

class dog implements Animal {
    public void cry() {
        System.out.println("멍멍!");
    }
}
public class Exam01 
    public static void main(String[] args) {
        Dog d = new Dog();
       
        d.cry();</code>
</pre>



