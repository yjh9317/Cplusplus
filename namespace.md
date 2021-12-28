namespace
===========
프로그래밍 과정에서 다른사람이 작성한 소스코드나 목적파일을 가져왔을 때 변수,함수,클래스등 이름이 같을 때  
컴파일하거나 링크할 때 오류가 발생할 수 있다.  
  
이렇게 이름이 같아서 충돌하는 경우를 막기 위해 자신만의 고유한 namespace를 사용해서  
같은 이름이여도 다른 namespace의 안에 있으면 서로 다른 변수로 취급된다.
  
namespace를 사용하는 방법은 namespace 키워드 뒤에 자신이 정할 namespace의 이름을 적고 중괄호{}를 묶으면 된다.<br><br><br>


ex)<br>
namespace Myspace{<br>
........<br>
}<br><br>

그리고 namespace안에 있는 식별자를 사용하기 위해서는 다음과 같이 사용한다  
<br>
ex) namespace::식별자  


<br><br>


std
=================
std는 2003년 C++ 표준에서 정한 표준 이름 공간으로, 모든 C++ 표준 라이브러리는 std 공간에 만들어져 있다.
그래서 응용 프로그램이 C++ 표준 라이브러리에서 선언된 식별자를 사용할 때 std::를 접두어 붙여서 사용해야 한다.  
예를 들어 C++에서의 표준 입출력을 사용하기 위해서는 밑에처럼 사용해야 한다.  
<br>
ex)<br>
std::cout<<"Hello World"<<std::endl; 
<br><br>

std안에 있는 식별자를 사용하려면 매번 std::를 접두어로 붙여서 사용하는데 이는 상당히 귀찮고 코드의 양을 늘린다.  
using 지시어를 사용해서 사용하려는 식별자를 선언하면 앞에 있는 std::를 생략해서 사용할 수 있다.  
<br>
ex)<br>
using std::cout;<br>
using std::endl;<br>
cout<<"Hello World"<<endl;<br>
