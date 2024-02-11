
## Swift에서 지역 범위와 전역 범위의 차이점을 설명하기
### Scope
해당 영역의 내부 또는 외부에서 필드의 영향을 받는 영역으로, **변수의 유효 범위**라고 할 수 있다.
> The area affected by the field, either inside or outside its region. -- [Apple Developers Documentation(SceneKit)](https://developer.apple.com/documentation/scenekit/scnphysicsfield/1388136-scope)

<br>

### Local Scope(지역 범위)
현재 존재하는 범위. 함수의 `{}` 블럭 안에 존재하는 변수로, 블럭 외부에서는 해당 변수에 접근할 수 없다.

<br>

### Global Scope(전역 범위)
모든 곳에 존재. 코드의 최상위 수준으로 함수나 클래스 외부에서 정의된 변수는 어디에서나 사용이 가능하다.

<br>

### 코드
```Swift
class Product {
    var kind = Kind.thing

    enum Kind {
        case food
        case thing
    }
}
```

- `Product` 클래스의 범위는 전역으로, 코드 어디에서나 Product 인스턴스를 만들 수 있다. 
- `Kind` 열거형의 범위는 해당 클래스인 `Product`로 제한된다. 클래스 외부가 아닌 내부에서만 `Kind`를 사용이 가능하다.

<br>

> 참고: [Scope and Context Explained in Swift
](https://www.appypie.com/scope-context-swift-how-to)