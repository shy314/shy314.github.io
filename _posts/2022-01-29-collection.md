---
layout: single
title : swift 공부 6일차 - 배열2
categories : swift
tags: [swift, collection]
toc: true
---

!나를 위한 기록!

[배열 첫번째 포스트로 이동](/swift/optional)

### Array

1) 배열 n번째 요소에 값넣기 
```swift
var numbers : [Int] = [1,2,5,7]
numbers[1] = 0
numbers[1...3] = [3,5,9]
```
2) 배열의 순서와 값 가져오기
```swift
for n in numbers {
    print(n)      
    //numbers 배열의 값을 순서대로 가져온다
}  
for (index, n) in numbers.enumerated() {
    print("index: \(index) , num: \(n)")  
    // n번째 값과 순서(index)를 가져온다 
}
```

3) 배열의 요소를 제거하는 다양한 방법
```swift
var numbers : [Int] = [1,2,5,7,9,13,16]

// 실제로 값이 제거되지 않음
numbers.dropFirst()     //[2, 5, 7, 9, 13, 16]
numbers.dropLast()      //[1, 2, 5, 7, 9, 13]
numbers.dropFirst(3)    //[7, 9, 13, 16]
numbers                 //[1, 2, 5, 7, 9, 13, 16]

// 값이 제거됨
numbers.remove(at: 0)
numbers                 //[2, 5, 7, 9, 13, 16]
numbers.removeFirst()
numbers.removeLast()
numbers                 //[5, 7, 9, 13]
numbers.remove(at: 2)   //[5, 7, 13]
numbers
numbers.removeAll()
numbers                 //[]
```

### Dictionary

1) 해당하는 키에 값넣기
```swift
var dict: [String:Int] = ["apple":1000, "kiwi":2000, "tomato":1500]

dict["apple"] = 1200
dict["kiwi"] = 1700
dict["tomato"] = nil
dict  //["apple": 1200, "kiwi": 1700]
```

2) 배열의 키와 값 가져오기
```swift
var dict: [String:Int] = ["apple":1000, "kiwi":2000, "tomato":1500]
for (f, p) in dict{
    print("물품: \(f), 가격: \(p)")
}    
//물품: tomato, 가격: 1500
//물품: kiwi, 가격: 2000
//물품: apple, 가격: 1000

for k in dict.keys{ 
    print("물품: \(k)")
}
//물품: tomato
//물품: apple
//물품: kiwi

for v in dict.values{
    print("가격: \(v)")
}
//가격: 1500
//가격: 1000
//가격: 2000
```

