friend
===========
클래스내에 다른 함수나 클래스를 friend로 선언하면 선언한 클래스나 함수에 접근할 수 있다.
먼저 함수를 friend로 선언하는 경우는 3가지가 있다.  
<br><br>
  * friend 함수 경우<br><br>
    * 전역 함수를 friend 선언<br><br>
    * 다른 클래스의 멤버 함수를 friend 선언<br><br>
    * 다른 클래스를 friend 선언  <br><br>



예시
===================
1.  
void Test();  

class Person{  
  int age;  
public:  
friend void Test();  
} 
<br><br>
첫번째 예시는 전역 함수를 friend 선언해서 넣은 경우이다.  
이 경우 Test함수는 Person의 멤버 함수처럼 Person의 모든 멤버에 접근할 수 있다.  

<br><br>
2.  
class Person_1{  
private:  
string name;
}  
<br><br>
class Person_2{  
  int age;  
public:  
void Naming(Person_1& p){  
p.name="Hi"  
}  
friend class Person_1();  
}  
<br><br>
두번째 예시는 class를 다른 클래스에서 friend로 선언한 경우이다.  
위의 경우는 Person_1의 private인 string 변수를 Person_2에서 접근해서  
Naming이란 함수로 Person_1의 객체인 p를 참조해서 이름을 바꿀 수 있게된다.  
