## Swift에서 print 기능의 적절한 사용법을 설명하기
> ```swift
> func print(_ items: Any…, separator: String = “ “, terminator: String = “\n”)
>```
- 본래 print는 파라미터가 3개인 함수이다.
- items과 terminator는 해당 파라미터 값이 디폴트로 설정되어 있지만, separator는 개발자가 필요할 때 적절히 사용한다.