---
layout: post
title: '[Swift] Optional Chaining을 사용하며 헷갈렸던 것들'
date: 2022/05/10/00:00
categories: Posts
---

## 변수로 사용될 때의 Optional Chaining

```swift
class Student {
    var age: Int = 0
}

var s1: Student? = Student()
s1?.age = 20    // Int형이 할당된다.
print(s1?.age)  // Optional(20)

var s2: Student?
s2?.age = 27    // nil로써 아무것도 실행되지 않음
print(s2?.age)  // nil
```

`Optional Chaining`을 사용한 변수에 어떤 값이 할당될 때는 하나라도 nil이 있으면 명령문이 무시된다.  
nil이 아닌 변수는 자동으로 언래핑 된다.

&nbsp;

참고한 강의 or 사이트  
\- [https://babbab2.tistory.com/32](https://babbab2.tistory.com/32)
