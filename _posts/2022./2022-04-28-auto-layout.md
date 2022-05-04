---
layout: post
title: Swift Auto Layout
date: 2022/04/28/00:00
categories: Posts
---

## Auto Layout

- 뷰의 크기와 위치를 제약조건(Constraint)을 기반으로 해서 동적으로 계산
- 상대적인 좌표
- Constraint의 모음

## Constraint(제약 조건)

1차 방정식(혹은 부등식)의 형태

![FirstItem.Attribute =(Relationship)= Multiplier \* SecondItem.Attribute \+ Constant](http://woin2ee.github.io/asset/images/Constraint-linear-equation.png)

- FirstItem : Constraint을 지정할 메인 오브젝트 **(*Required*)**
  - Attribute : FirstItem의 Auto Layout 속성
- RelationShip : 좌변과 우변의 관계 (=, <=, >=)
- Multiplier : 좌변과 우변의 비율을 조정하기 위한 곱셈 값
- SecondItem : Constraint을 지정할 기준 오브젝트 **(*Optional*)**
  - Attribute : SecondItem의 Auto Layout 속성
- Constant: 상수

 Ex) Label.top = 1 * Safe Area.top + 50

## Auto Layout Attribute

![Auto Layout Attributes](http://woin2ee.github.io/asset/images/Auto-Layout-Attributes.png)

- Width
- Height
- Top
- Bottom
- Baseline
- Leading
- Trailing
- CenterX
- CenterY
- Horizontal
- Vertical

## Safe Area

Application이 상태바, 네비게이션바, 탭바를 가리는 것을 방지하는 영역

## Priority (우선도)

### Intrinsic Content Size

`Auto Layout`에 변경되기 전 뷰의 원래 크기

### Constraint Priority

Constraint가 충돌하는 경우 적용할 우선 순위 값  
기본 **1,000(무조건 적용)**으로 설정되어있고, **750(우선순위높음)**, **500(중간)**, **250(낮음)**의 값을 갖는다.

- #### Contents Hugging

  : 뷰가 `Intrinsic Content Size` 보다 커지지 않도록 함

- #### Contents Compression Resistance

  : 뷰가 `Intrinsic Content Size` 보다 작아지지 않도록 함
