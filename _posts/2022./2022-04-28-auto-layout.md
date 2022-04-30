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

![FirstItem.Attribute =(Relationship)= Multiplier \* SecondItem.Attribute \* Constant](http://woin2ee.github.io/asset/images/Constraint-linear-equation.png)

- FirstItem : Constraint의 대상이 되는 두 뷰 중 하나입니다. 뷰 혹은 레이아웃 가이드 객체만이 가능하며, 반드시 지정되어야만 합니다.
  - Attribute : FirstItem에서 실제로 Constraint에 영향을 받는 속성입니다.
- RelationShip : 좌변과 우변의 관계입니다. 등호(=), 등호가 붙은 부등호(>=, <=)의 3가지 경우가 가능합니다.
- Multiplier : SecondItem.Attribute에 곱해지는 부동 소수점 타입의 계수입니다.
- SecondItem : Constraint의 대상이 되는 두 뷰 중 나머지 하나입니다. FirstItem과 다르게, 지정되지 않는 것이 가능합니다.
  - Attribute : SecondItem에서 실제로 Constraint에 영향을 받는 속성입니다.
- Constant: SecondItem.Attribute에 더해지는 부동 소수점 타입의 상수

 Ex) Label.top = 1 * Safe Area.top + 50

## Safe Area
