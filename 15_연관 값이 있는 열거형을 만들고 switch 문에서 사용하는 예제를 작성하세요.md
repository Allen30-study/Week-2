## 연관 값이 있는 열거형을 만들고 switch 문에서 사용하는 예제를 작성하세요.
```swift
enum Pets {
    case nana(species: String, age: Int, hobby: String, from: String)
    case lunar(species: (String, String), age: Int, hobby: String, from: String)
    case ruby(species: (String, String), age: Int, hobby: String, from: String)
}

let nana: Pets = .nana(species: "dog", age: 15, hobby: "playing with ball", from: "vetarinary clinic")
let lunar: Pets = .lunar(species: ("cat", "tabby"), age: 8, hobby: "napping", from: "street")
let ruby: Pets = .ruby(species: ("cat", "chaos"), age: 3, hobby: "fishing with playstick", from: "street")

func describePet(pet: Pets) {
    switch pet {
    case let .nana(species, age, hobby, from):
        print("Nana is a \(species) aged \(age), enjoys \(hobby), and is from \(from).")
    case let .lunar(species, age, hobby, from):
        print("Lunar is a \(species.0) (\(species.1)) aged \(age), enjoys \(hobby), and is from \(from).")
    case let .ruby(species, age, hobby, from):
        print("Ruby is a \(species.0) (\(species.1)) aged \(age), enjoys \(hobby), and is from \(from).")
    default:
        break
    }
}
```