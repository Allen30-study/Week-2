## 문자열 배열을 가져와 문자열(String)을 키로, 길이를 값으로 사용하여 딕셔너리를 반환하는 함수를 구현합니다.
```swift
func mkDict(_ array: [String]) -> [String: Int] {
    var dict: [String: Int] = [:]
    
    for str in array {
        dict[str] = str.count
    }
    
    return dict
}

print(mkDict(strArrray))
```