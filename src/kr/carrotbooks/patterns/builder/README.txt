Builder Pattern
	- 여러 객체를 포함하는 객체(Composite Object)의 생성을 담당하는 부분을 본체에서 분리해 내는 패턴
	  서로 다른 대상을 같은 생성자를 이용해서 생성할 수 도 있다.
	- 예제에서 사용된 개념은 다음과 같다:
		- 만들어질 객체를 포함하는 클래스를 빌더라 한다.
		- 생성된 빌더를 디렉터에게 넘겨준다
		- 디렉터는 필요한 순서에 따라 내부 객체들을 생성한다
		- 빌더를 통해 만들어진 객체를 얻어낸다.
	- 이때 추상 클래스 / 인터페이스를 이용함으로서 하나의 디렉터를 이용하여 같은 처리를 필요로 하는
	   다른 클래스의 객체를 생성해 내도록 할 수 있다.

IGOFBuilder		- 빌더의 추상 클래스 / 인터페이스
	ConcreteBuilder - 빌더의 구현 클래스
Director		- 객체 생성을 시행하는 클래스. 빌더를 인자로 받는다. 생성 진행 순서를 다룬다.
Product			- 실제로 생성되는 객체의 클래스
				  Builder의 getResult() 메소드의 리턴값이 된다. 
				   패턴의 다이어 그램에는 표시되어 있지 않은 클래스
