---
layout: post
title:  "[운영체제] 👩🏼‍💻 2. 운영체제의 역사에 대해 알아보자"
date:   2020-08-16 18:34:10 +0700
categories: [operating system]
---

> [경성대학교 양희재 교수님 - 운영체제의 역사](http://www.kocw.net/home/cview.do?lid=31dfd5c232f54591) 을 보고 포스팅한 것입니다.

# [👩🏼‍💻 2. 운영체제의 역사에 대해 알아보자]

✍🏻 [이 블로그의 다른 포스팅 - 운영체제가 뭘까?](https://choheeis.github.io/newblog//articles/2020-05/OSstart) 를 먼저 읽어보고 오는 것이 좋다!

## 1️⃣ 최초의 컴퓨터(초기 컴퓨터의 동작 방식)

최초의 컴퓨터는 무려 1940년대 말에 발명되었다. 

<img width="393" alt="01" src="https://user-images.githubusercontent.com/31889335/100973221-81cfde80-357d-11eb-93a2-ca535e6aced7.png">

초기 컴퓨터는 위와 같은 모습을 하고 있었으며 크기 자체가 너무 커 건물 하나를 차지하는 정도였다.

그 중에서도 입력장치인 카드리더기가 차지하는 공간이 가장 컸다.

초기 컴퓨터의 입력은 천공카드였다. 천공카드는 주로 시험을 볼 때 사용하는 OMR 카드와 비슷했지만 OMR 카드에서 검정색으로 칠하는 동그란 부분을 구멍을 뚫어 표현하는 방식이였다.

아래 사진이 천공카드이다! 예를 들어, y=x+3을 표현하기 위해 y에 해당하는 자리에 구멍을 뚫고, =에 해당하는 자리에 구멍을 뚫고, x자리와 +자리, 3자리에 각각 구멍을 뚫는 형식이라고 생각하면 된다.

<img width="1343" alt="02" src="https://user-images.githubusercontent.com/31889335/100973230-86949280-357d-11eb-9dee-8b7bbe5a8579.png">

입력장치인 카드리더기가 읽은 천공카드의 내용이 메모리에 저장되고 나면 프로세서가 메모리에서 읽은 명령어들을 읽어 처리하였다.

이랬던 초기 컴퓨터가 명령어들(프로그램)을 처리할 때 도와주는 컴파일러라는 프로그램도 존재했다.

메모리에 천공카드에서 읽은 명령어들을 저장한 뒤에 컴파일러 프로그램(명령어들)을 표현한 천공카드를 카드리더기에 올린다.

컴파일러 프로그램을 추가로 카드리더기에 올리는 이유는 입력받은 프로그램을 프로세서가 처리하기 위해서 명령어들이 기계어로 변환되어야 하기 때문이다.

컴파일러 프로그램을 나타내는 천공카드를 카드리더기에 읽히게 되면 메모리에 컴파일러가 올라가게 되고 이 컴파이러가 이미 메모리에 올라와있는 프로그램들을 기계어로 번역을 하게 된다.

이제서야 기계어로 번역된 프로그램을 프로세서가 처리하게 되는 것이다.

그 당시에는 모니터라는 것이 없었기 때문에 처리기가 처리한 내용을 프린터를 사용해 종이에 찍어 출력하였는데 초기 프린터는 망치(해머)로 종이를 두들겨서 출력하는 방식이였다.

이러한 입력부터 출려까지의 모든 과정을 컴퓨터 전문가인 Operator 라고 불리는 사람이 수행하고 관리하였다.

여기서 알 수 있는 사실은 초기 컴퓨터가 등장했던 1940~1950년대에는 운영체제가 없었다는 것이다!

<br>

## 2️⃣ 최초의 운영체제가 등장하다! Batch Processing System의 등장

위에서 공부한 내용처럼 초기의 컴퓨터는 사람이 일일이 천공카드를 카드리더기에 올리고 컴파일러 프로그램도 올려야했기 때문에 불편한 점이 많았다.

기술이 점점 발전하면서 "이러한 일들을 사람이 하지 않고 컴퓨터 스스로 하게 할 수 없을까?" 라는 생각을 그 당시 컴퓨터 분야를 연구하는 사람들이 하게 되었다.

이 생각으로 인해 __Batch Processing System__ 라는 기술을 발명하게 되었다!

Batch는 꾸러기, 묶음이라는 뜻을 가지고 있다. 즉, __Batch Processing 은 묶어서 처리한다__ 라는 의미이고 우리말로는 __일괄처리__ 라고 한다.

위에서 알아본 내용 중 그 당시 Operator라는 사람은 프로그램 하나를 실행하고 싶을 때마다 컴파일러 프로그램도 카드리더기에 직접 올려야했고 그 외에 링킹 프로그램 올리기, 로딩 프로그램 올리기 등 여러가지 할 일들이 많았었다.

컴파일러, 링킹, 로딩 프로그램 등을 카드 리더기에 올리는 일련의 과정을 사람이 아닌 컴퓨터가 일괄적으로 처리해주는 프로그램을 만들어 이 프로그램 하나만 메모리에 올림으로써 사람이 할 일을 줄이자! 라는 개념을 탑재한 시스템이 Batch Processing System이다.

이 일련의 과정을 처리해주는 프로그램을 resident(레지던트) monitor 이라고 불렀다.

> resident 라는 단어는 '상주한다' 라는 의미를 가지고 있다.

결국 __Batch Processing 시스템이 최초의 운영체제__ 였던 것이다.

## 3️⃣ Multi-Programming System의 등장

최초의 운영체제인 Batch Processing System 이 등장한 후, 기술의 발전이 계속되어 하드디스크가 발명되게 되었고, 진공관 형태였던 프로세서(CPU)도 트랜지스터를 이용하여 반도체 형태로 만들어지게 되었다.

이렇게 기술이 한창 발전하고 있을 시기에 컴퓨터 분야에서도 한 가지 불편함을 해결하고자 하려는 노력이 생겨나게 되었다.

초기 컴퓨터는 운영체제와 단 한 개의 프로그램만 메모리에 올라갈 수 있는 구조였다. 즉, 최초의 운영체제인 Batch Processing 시스템과 실행시킬 프로그램 한 개만 메모리에 올라갔다는 것이다.

예를 들어, 초기 컴퓨터가 실행시킬 다음과 같은 간단한 프로그램이 존재할 때 동작 과정을 살펴보자.

c++ 언어로 작성하였지만 입력(cin)은 카드리더기로, 출력(print)은 프린터로 된다고 상상하자!

~~~c++
#include<iostream>
using namespace std;

int main(){
    int a = 0;
    int b;
    cin>>b;
    for(int i = 0 ; i < 10 ; i++){
        a += b + 1;
    }
    print(a);
}
~~~

변수를 선언하고 산수 계산을 하는 것은 프로세서(CPU)의 역할이다.

하지만 cin>>b; 와 print(a); 명령은 프로세서가 처리하는 것이 아니라 입력장치인 카드리더기와 프린터의 역할이다.

이렇게 하나의 프로그램이 실행될 때는 프로세서와 입/출력 장치들이 번갈아가면서 동작하게 된다.

하지만 그 당시의 사람들이 이러한 동작 과정에 존재하는 문제 하나를 인식하게 되었다!

카드리더기나 프린터가 작동하고 있을 동안 프로세서는 할 일이 없어지게 된다. 입출력 작업이 끝나고 다시 자신이 해야할 일이 올 때까지 아무 일도 하지 않은채 가만히 있는다는 사실을 문제로 인식하였다.

프로세서가 아무일도 하지 않는 현상을 __cpu idle__ 이라고 부른다.

이러한 점을 문제라고 인식한 이유는 초기 컴퓨터는 크기도 클 뿐더러 가격도 엄청 비쌌기 때문에 비싼 자원 중 하나인 프로세서가 아무 일도 하지 않은채 가만히 살아있기만 한다는 것은 비용적인 측면에서 큰 손해였기 때문이다.

심지어 너무 비싼 가격 때문에 그 당시 우리나라에는 컴퓨터가 없었다..

또한 프로세서는 처리 속도가 빠르지만 입/출력 장치인 카드리더기와 프린트는 처리 속도가 느려 오래 걸렸기 때문에 시간적인 측면에서도 손해였다.

그래서 사람들이 생각한 방법은 __메모리에 단 한 개의 프로그램만 올릴 수 있는 것이 아니라 여러 프로그램을 올릴 수 있도록 기술을 개발하자!__ 였다.

메모리에 여러 프로그램을 올리게 됨으로써 얻는 장점은 다음과 같았다.

<img width="834" alt="03" src="https://user-images.githubusercontent.com/31889335/100973240-898f8300-357d-11eb-8ed5-0e0723fa5084.png">

프로그램 1에서 입출력장치가 실행되어야 하는 작업을 만난다면 프로세서는 다음 프로그램인 프로그램 2의 계산 부분을 처리하면 된다.

또 프로그램 2에서 입출력 작업을 만난다면 프로그램 3의 계산 부분을 처리하면 되는 것이다.

만약 프로그램 3에서 입출력 작업을 만난다면 다시 앞으로 돌아와서 입출력 작업이 완료되어 있는 프로그램 1의 나머지 계산 작업을 프로세서가 하게 된다.

즉, 프로세서가 아무 일도 하지 않은 채 기다리기만 하는 일이 없어지게 된 것이다!

그 당시 컴퓨터 분야를 연구하던 사람들은 이러한 방법으로 cpu idle 시간을 대폭 줄이고, cpu 사용률을 증가시킬 수 있다고 생각하였다.

이렇게 메인 메모리에 하나의 프로그램이 아닌 여러 개의 프로그램을 올릴 수 있도록 개발된 시스템을 __Multi-Programming System(다중 프로그래밍 시스템)__ 이라고 부른다.

Multi-Programming System의 등장으로 단지 메인 메모리에 프로그램을 여러개 올릴 수 있게 하는 기술만 발전했을까? 아니다.

자연스럽게 __CPU 스케줄링__ 이라는 기술도 등장하게 되었다.

CPU 스케줄링이란 위 예시에서 CPU 작업을 몇 번째 프로그램부터 하게 하고, 어떤 순서로 CPU 작업을 옮겨다녀야 성능이 높아지는지에 대한 개념이다.

위 그림 예시에서 프로그램 1 -> 프로그램 2 -> 프로그램 3 순서로 CPU 작업을 옮겨다닐 때의 처리 속도와 프로그램 2 -> 프로그램 1 -> 프로그램 3 순서로 CPU 작업을 옮겨다닐 때의 처리 속도가 달라지기 때문이다.

CPU 스케줄링 기술 뿐만 아니라 __메모리 관리__ 부분에서도 기술들이 등장하게 되었다.

Multi-Programming System의 등장 전에는 메인 메모리에 하나의 프로그램만 올라가 있었기 때문에 상관이 없었지만 여러 개의 프로그램이 올라갈 수 있게 되면서 여러 프로그램을 메인 메모리에 어떻게 배치시키는 것이 좋은지에 대해서도 고민하게 되었기 때문이다.

메인 메모리에 프로그램이 올라온 순서대로 다닥다닥 붙여서 위치시키는 것이 좋은지 프로그램마다 띄엄 띄엄 떨어뜨려서 위치시키는 것이 좋은지 등을 고민하게 되었다.

더불어 여러 프로그램 중 두 개의 프로그램을 사용자가 종료시켜 메인 메모리 중간 중간에 빈 공간이 생긴 경우에, 곧이어 실행되는 새로운 프로그램을 빈 공간 중 어디에 위치시키는 것이 좋을까? 어떻게 위치시켜야 현재 실행되고 있는 프로그램의 메모리 영역을 침범하지 않을까? 등에 대한 고민도 존재했다.

즉, Multi-Programming System의 등장으로 자연스럽게 부가적인 기술들이 개발되어야 했고, 실제로 개발되었다는 것이다.

Multi-Programming System이 등장하여 이러한 고민들을 할 당시가 1960년대이다.

1960~1970년대에는 모니터, 키보드가 발명되어 카드리더기와 프린터를 대신할 새로운 입출력장치도 등장했다.

## 4️⃣ Time-Sharing System(시간 공유 시스템)의 등장

Multi-Programming System을 지원하는 운영체제의 등장과 더불어 1970년대에는 모니터, 키보드가 발명되어 더 이상 카드리더기를 통해 입력받고 프린터를 통해 출력할 필요가 없어졌다.

사용자가 키보드로 입력하면 모니터에서 컴퓨터가 처리한 결과를 볼 수 있었기 떄문에 사용자들은 컴퓨터와 Interactive(상호작용)하며 대화한다고 느끼게 되었다.

그 당시에 이러한 대화형 컴퓨터를 지원하려고 하다보니 조금 괴의한 모습의 컴퓨터가 등장했는데 바로 아래와 비슷한 모습이다.

<img width="330" alt="04" src="https://user-images.githubusercontent.com/31889335/100973241-898f8300-357d-11eb-8d44-8921e51b9b2b.png">

그 당시의 컴퓨터는 크기도 크고 아주 비쌌기 때문에 하나의 컴퓨터에 키보드와 모니터만 여러개 붙여서 여러 명이 하나의 컴퓨터와 대화할 수 있게 하는 모습의 컴퓨터가 등장하였다.

<img width="967" alt="05" src="https://user-images.githubusercontent.com/31889335/100973242-8ac0b000-357d-11eb-86f5-718e3475586d.png">

위 그림과 같이 하나의 컴퓨터가 존재하고 여러 대의 __단말기(영어로는 Terminal)__ 이 붙어있는 모습이였다.

이런 모습의 대화형 컴퓨터가 등장하니 Multi-Programming System을 지원하는 운영체제가 대화형 컴퓨터에서는 잘 동작하지 않는 문제가 발생하였다.

대화형 컴퓨터의 운영체제가 Multi-Programming System 운영체제이고 위 그림처럼 하나의 대화형 컴퓨터를 사용하는 5개의 단말기(5명의 User 라고 보아도 무방하다)가 존재한다고 가정해보자.

또, 한 사람당 하나의 프로그램만 실행시킬 것이라고 가정해보자.

그렇다면 Multi-Programming System을 지원하는 메인 메모리에는 운영체제, User1이 실행시킨 프로그램, User2이 실행시킨 프로그램, User3이 실행시킨 프로그램, User4가 실행시킨 프로그램, User5가 실행시킨 프로그램이 올라가 있을 것이다.

CPU가 User1부터 순서대로 프로그램을 옮겨다니면서 계산 작업을 하는 스케줄링을 가지고 있다고 하면 User1에서 계산 작업을 하고 있을 동안 User2, User3, User4, User5의 프로그램에서는 어떠한 계산 작업도 실행되지 않고 기다리는 상황이 될 것이다.

즉, 각각의 사용자는 다른 사용자 프로그램의 입출력 작업을 만나 CPU가 자신의 프로그램으로 넘어올 때까지 기다려야 했고, 만약 자신의 프로그램으로 넘어온 CPU가 입출력 작업을 만난다면 또 다시 다른 사용자의 프로그램으로 CPU가 옮겨간다는 문제가 발생한 것이다.

따라서 하나의 컴퓨터를 여러 단말기가 사용하려면 기존의 Multi-Programming System 을 지원하는 운영체제 방식은 곤란하다는 결론이 났다.

이를 해결하기 위해 __Time-Sharing System(시간 공유 시스템)__ 이라는 개념이 등장했는데 이것에 대해 차근 차근 알아보자.

기존의 Multi-Programming System에서 프로그램 간 CPU 이동이 발생하려면 CPU 작업이 입출력 작업을 만나야 했다.

하지만 Time-Sharing System에서는 프로그램 간 CPU 이동이 입출력 작업 만남의 여부에 달려있지 않고 정해진 고정 시간이 지나면 강제적으로 이동하는 시스템이다.

<img width="544" alt="06" src="https://user-images.githubusercontent.com/31889335/100973245-8dbba080-357d-11eb-96f2-143a90d096f4.png">

위 그림처럼 CPU는 __아주 짧은 시간__ 인 0.01초나 0.001초 동안 User1이 실행시킨 프로그램의 계산 작업을 수행한다. 이 짧은 시간이 지나면 바로 User2가 실행시킨 프로그램으로 이동해 같은 시간 동안 계산 작업을 수행하고, 마찬가지로 이 시간이 지나면 User3이 실행시킨 프로그램으로  이동해 계산 작업을 수행하는 방식이다. User3에서의 작업 시간이 지나면 다시 User1이 실행시킨 프로그램으로 이동해 같은 시간 동안 계산 작업을 한다.

만약 하나의 프로그램에서 CPU 작업을 하는 짧은 시간이 0.01초라고 가정했을 때 1초 동안 3개의 프로그램은 각각 대략 33번정도 CPU 작업을 실행하게 된다.

CPU가 매우 짧은 시간동안 프로그램을 옮겨다니기 때문에 사용자 각각의 입장에서는 자신이 CPU를 기다리는 시간이 훨씬 줄었다고 생각하게 될 것이다.

그래서 각 사용자는 여러 단말기가 하나의 컴퓨터를 나눠 사용하고 있는 것이 아닌 자기 혼자 하나의 컴퓨터를 사용하고 있다고 느끼게 될 것이다.

이것이 바로 __Time-Sharing System__ 이다. 이 시스템을 지원할 수 있도록 개발된 첫 운영체제가 바로 __Unix(유닉스)__ 였다.(1960년대 후반에 등장)

이러한 Time-Sharing System의 등장으로 자연스럽게 추가 기술들이 발전할 수밖에 없었다.

예를 들어, 위에서 예시로 든 그림에서는 User가 5명 뿐이지만 더 많은 수의 User가 하나의 컴퓨터에 붙어 사용하게 된다면? 

메인 메모리에 그 만큼 많은 수의 프로그램이 올라가게 되어 결국 메인 메모리의 용량보다 많은 용량이 필요하게 될 수도 있다.

이 문제를 해결하기 위해 보조 저장소로 사용되던 하드디스크 중 일부 용량을 메인 메모리 마냥 사용할 수 있도록 하는 기술이 개발되었다.

CPU 입장에서는 메인 메모리인 마냥 사용되는 하드 디스크의 일부도 메인 메모리처럼 보이게 되었는데 이것을 __가상 메모리(Virtual Memory)__ 라고 한다.

또한 하나의 컴퓨터에 붙어서 프로그램을 실행시키는 각각의 User는 공유하는 컴퓨터를 통해 서로 자기들끼리 데이터를 주고 받을 수 있는 기술도 등장하게 되는데 이것을 __프로세스간 통신__ 이라고 한다.

1960년대에 등장한 Time-Sharing System은 현재의 운영체제에도 탑재되어 있는 시스템이다.

예전과 달라진 점은 예전에는 한 대의 컴퓨터를 여러 User가 공유하는 모습이였지만 현재는 한 대의 컴퓨터를 한 명의 User가 사용하는 모습이라는 점이다.

하지만 한 명의 User가 사용하는 한 대의 컴퓨터의 운영체제도 여러 프로그램을 동시에 실행시키는 것처럼 보이기 위한 방법으로 Time-Sharing System을 지원하고 있다.

## 5️⃣ 운영체제 역사 최종 정리

1. 처음에는 __운영체제가 없는 컴퓨터__ 였다. Operator라는 사람이 일일이 프로그램을 카드 리더기에 올리고, 컴파일러를 카드 리더기에 올려야하는 문제가 발생했다.

2. 1번 작업들을 일괄적으로 처리하기 위해 __Batch-Processing System이 등장__ 했다. 하나의 프로그램만 실행시킬 경우 cpu idle 문제가 발생했다.

3. __Multi-Programming System이 등장__ 했다. 이 때 키보드와 마우스가 발명되었다.

4. 한 대의 컴퓨터에 여러 단말기가 붙은 대화형 컴퓨터가 등장하였고, __Time-Sharing System이 등장__ 하였다.

이렇게 운영체제가 지원하는 시스템이 발전하면서 자연스럽게 부가적인 기술들도 개발되었고, 이 기술들을 적용시키면서 운영체제 자체도 더욱 발전했고 성능도 좋아졌다.

이런 역사를 거쳐 현대의 다양한 컴퓨터(PC, 노트북, 태블릿, 스마트폰, 임베디드 시스템)에는 Time-Sharing System이 탑재되어 있다.

# 끝!