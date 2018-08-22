# SwiftStudy
Swift文法概要(整理中)

#Swift tutorials 번역

1. 오늘날에  Objective_C 밖에 없던 시절, 캡슐화는 클래스에서 사용할 때 제한적이었다. 그런데, 모뎀
IOS와 MAC이 프로그래밍되고 3개의 선택지가 (Enums, structs, classes) Swift에 생기게 되었다.

프로토콜과 결합되면서 이 타입들은 엄청난 일을 만들게 끔 가능해지게 된다. 단순한 많은 일들이 공유될
대까지 말이다.그 타입들은 또한 중요한 차이점들을 가지게 되는데,

    ==이 튜토리얼의 목표
1) classes, structs, Enums를 쓰기에 약간의 경험을 줄것이다
2) 위에 것들을 사용할 떄 약간의 직관력을 얻게 된다
3) 각각의 작업들이 어떻게 이루어질지 알게 된다.

이런 전제조건에서, 이 튜토리얼은 약간의 Swift와 객체지향의 프로그래밍 경험을 줄것이라 추정한다.

- 타입의 모든 것

2. Swift는 safety(안정성), speed(빠름), simplicity(간단함)이라는 3개의 장점을 가지고 있다.

안정성은 암시적, 실수로 실행되는 미친코드의(변질된 메모리와 산출되는 연산) 버그를 발견하는 것은 어렵다.Swift는 그 작업에 관해 안정적으로 만들어 줄것이다 이것은 확실한데, 당신이 버그를 발견하고 코치는 시간보다 구동하는 시간이 보다 많을 것이기 때문이다

더욱이 Swift는 당신이 당신의 일에 전념하게끔 전적으로 도와줄것이며, 잘 활용한다면 당신의 코드를 실행시키는데 엄청나게 빠른 그리고 싸게 도와줄 것이다. Swift 언어의 중심은 단순함과 정규성인데 아주 놀랍고 감사하게도 작은 숫자의 개념들만 있을 뿐이다, 상대적으로 단순한 규칙 뿐임에도 당신은 놀라운
일을 할 수 있을 것이다

그것이 가능하게 하는 것은 Swift의 타입 시스템때문이다
			
				Types
	Named						Compound

protocol    eunm    struct    class		tuple		   function
	   (      model types      )

Swift 타입들은 6개밖에 없음에도 강력하다. 그렇다, 많은 다른 언어들과 달리(수십가지의 타입을 가진) 
Swift는 오직 6개만 가진다

그것들은 크게 4개가지 타입으로 이루어져있는데 : protocol, enum, struct, class. 그리고 2개의 Compound는 : tuple, function
그 타입들은 또한 다른 당신이 생각하는 기본적 타입들 : Bool, Int, Uint, Float, Double, Char, String etc.
그런데 실제로 코드를 짤때 Named 타입과 Swift의 기본적인 라이브러리의 일부분으로 만들 수 있다는 것이다
해당 튜토리얼은 Named타입으로 구성되는 3가지(enum, struct, class)에 주안점을 두고 있다.

3. 시작해보자

Xcode에 메뉴얼에 따라 새로운 파일을 만들어보자, 그리고 파일 이름은 Shapes로 설정, 그리고 platform은 OS X,
Next를 눌러주고 경로를 save 하자, 만들어진 파일은 저장한다, 확실하게 파일을 만들고 따라해보자 