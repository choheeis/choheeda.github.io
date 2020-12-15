---
layout: post
title:  "[안드로이드] Resource 관리하기 - dimension(크기 단위)이란?"
date:   2020-12-15 18:34:10 +0700
categories: [안드로이드]
---

## 1️⃣ 안드로이드 뷰 크기 설정할 때 사용하는 단위들

✍🏻 [Android Developer 도큐먼트 - 리소스 유형, Dimenstion](https://developer.android.com/guide/topics/resources/more-resources#Dimension)을 참고하여 작성합니다.

안드로이드 개발을 할 때 뷰(View)의 크기를 xml 파일에서 설정해주어야 한다.

이 때 안드로이드에서 지원하는 __크기 단위(측정 단위)__ 는 여러 가지가 있는데 각 단위에 대해 알아보자.

* __dp(Device Independence Pixel)__

    dp의 의미는 __디바이스에 독립적인 픽셀__ 이라는 의미이다. 디바이스에 독립적인 픽셀이라는 말에 대해서 이해하기 위해 조금 더 살펴보자.

    휴대폰 디바이스는 화면 사이즈가 같은 기기라도 화면의 밀도는 다를 수 있다.

    밀도가 다르다는 말은 인치당 도트(화소) 수가 디바이스마다 다르다는 것이다.

    <img width="625" alt="01" src="https://user-images.githubusercontent.com/31889335/102197992-31556b00-3f05-11eb-99bd-5eb31f58d7c2.png">

    위 그림은 같은 인치당 도트 수가 다를 때 보이는 화면 차이를 나타낸다. 도트 수가 많을수록 화질이 좋아짐을 알 수 있다.

    __해상도__ 라는 용어도 디바이스 화면의 가로, 세로에 몇 개의 도트가 존재하는가를 나타내는 용어이다.(예 - 1,920 x 1,080 해상도)

    즉, 휴대폰 디바이스는 화면 사이즈가 같아도 휴대폰 스펙에 따라 도트 수가 다를 수 있다는 것을 알아야 한다.

    안드로이드는 화면 밀도가 다른 다양한 휴대폰 디바이스를 지원하기 위해 __dp__ 라는 측정 단위가 존재한다.

    __dp__ 는 __화면의 물리적인 밀도에 기반한 상대적인 픽셀__ 이다.

    예를 들어, 밀도가 낮은 화면에서 2dp x 2dp 이미지와 밀도가 높은 화면에서 2dp x 2dp 이미지는 눈으로 보았을 때는 사이즈가 같아보인다.

    하지만 실제로 2dp x 2dp 이미지에 사용된 픽셀 수는 다르다.

    밀도가 높은 화면의 2dp x 2dp 이미지에 사용된 픽셀 수가 더 많게 된다.

    따라서 다양한 화면 밀도에 대응하기 위해 뷰의 width, height 측정 단위를 dp로 사용할 수 있다.

    즉, dp를 통해 다양한 기기에서 UI 요소의 크기에 일관성을 부여할 수 있게 된다.

* __sp__

> 추가로 이어서 작성하기

## 0️⃣ 먼저 읽어보고 올 것!

[이 블로그의 다른 포스팅 - 안드로이드 Resource에 대해서](https://choheeis.github.io/newblog//articles/2020-04/AppResource) 를 먼저 읽어본 후, Resource가 무엇인지 알아보고 오자!

## 1️⃣ res/values 폴더 안에 존재하는 것들

 이거 읽고 이어서 작성하기!