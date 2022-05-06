---
layout: post
title: '[Swift] TableView의 contentConfiguration 사용법'
date: 2022/05/06/18:50
categories: Posts
---

## textLabel & imageView 등을 사용하던 기존 방법

```swift
func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> 
  UITableViewCell {
  let cell = UITableViewCell(style: .default, reuseIdentifier: "myCell")
  cell.textLabel?.text = "\(indexPath.row)"
  return cell
}
```

- `textLabel`이 `Deprecated`됨에 따라 cell을 설정할 다른 방법이 필요해짐

## contentConfiguration을 사용한 방법

```swift
func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> 
  UITableViewCell {
  let cell = UITableViewCell(style: .default, reuseIdentifier: "myCell")
  
  // UIListContentConfiguration 객체 생성
  var content = cell.defaultContentConfiguration()
  // var content = UIListContentConfiguration.cell() // 이렇게도 사용 가능

  // Configure content.
  content.image = UIImage(systemName: "star")
  content.text = "\(indexPath.row)"
  // Customize appearance.
  content.imageProperties.tintColor = .purple
  
  // contentConfiguration 지정
  cell.contentConfiguration = content

  return cell
}
```

- **`contentConfiguration`** : `UIContentConfiguration` Protocol을 준수하는 property. cell의 현재 설정을 나타낸다.
![contentConfiguration](http://woin2ee.github.io/asset/images/contentConfiguration.png)

- **`defaultContentConfiguration()`** : `UIListContentConfiguration` 타입의 기본 설정 객체를 만들어 반환해준다.

- **`UIListContentConfiguration`** : 리스트 형식으로 보여주는 content view의 contentConfiguration 를 담당하는 구조체. `UIContentConfiguration` Protocol을 준수하고 있다. 객체를 생성하는 static 메소드를 여러개 가지고 있고, text & image 등을 설정하는 property들을 가지고 있다.
![UIListContentConfiguration-Creating-Default-Cell-Configurations](http://woin2ee.github.io/asset/images/UIListContentConfiguration-Creating-Default-Cell-Configurations.png)
![UIListContentConfiguration-Customizing-Content](http://woin2ee.github.io/asset/images/UIListContentConfiguration-Customizing-Content.png)

