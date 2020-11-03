# Capstone Design

 + Project-name: Detecting smoking outside the smoking area using object detection
 + Team-name: 님아, 그 선을 넘지마오. (Don't Cross the line)
 + with: 김태현, 김상현, 박지훈, 박현우.
 + This project is the graduation work of the 2nd semester of the 4th grade of the Department of Computer Science at Kyunggi University.

<br>

## Introduction
 + 본 작품은 흡연 구역 밖의 흡연자들을 감지하여 관리자에게 실시간으로 흡연자의 정보를 제공하는 웹 어플리케이션 서버를 활용한다.
 + 본 프로젝트에서는 금연구역 경계선을 영상 처리 기법을 활용하여  명확하게 정의하고,  지정된 금연구역에서 흡연 하는 사람을 객체 탐지를 활용하여 구별하고 탐지한다.
 + 전체적인 진행 절차는 영역 정의 -> 객체 탐지 -> 얼굴 인식 -> 신원 정보 조회 및 메일링의 단계로 구성된다.

  1. 영역정의 : 주어진 영상 내에서 흡연 구역을 명확한 경계선을 바탕으로 지정하는 단계로써, 영상 처리 기법을 이용하여 영상의 첫 부분을 캡처 한 뒤 해당 부분에서 마우스 클릭 이벤트를 활용하여 영역을 정의하고 해당 영역의 좌표 값을 저장하는 역할을 한다.
  2. 객체탐지 : 어진 영상 안에서 인스턴스 단위로 정의된 객체가 존재하는지, 존재 한다면 경계 박스(Bounding Box)를 이용해 각 객체의 공간적인 위치와 카테고리를 반환하는 것이다. 본 프로젝트에서는 영역 제안 (Region-proposal)과정이 생략 되었고, 단일 단계의 과정을 거쳐 Detection을 수행하는 One-stage detection(YOLO계열)으로 구현 하였다.
  3. 얼굴인식 : 디지털 이미지를 통해 각 사람을 자동으로 식별하는 프로그램으로 얼굴 탐지(Face Detection)후, 특징 추출을 하고, 기존에 안면 데이터베이스에 저장되어 있는 사진에서 얻어진 특징과 추출이 된 특징 값을 서로 비교하여 사람의 신원을 파악한다. 
  4. 신원 정보 조회 및 메일링 : 마지막으로 신원 정보를 조회하여 데이터베이스에 저장된 해당 적발자의 증거 사진을 첨부하여, 해당 적발 대상에서 메일을 보내는 방식으로 시스템이 구성되어 있다. 여기서 HTML의 Mailto는 HTML의 링크 타입에 속한다. 이 링크는 사용자의 컴퓨터에 깔려 있는 메일 클라이언트를 실행시켜서 E-Mail을 보낼 수 있게 해주는 태그이다. 
     ![process](https://user-images.githubusercontent.com/62137510/92366301-ef5fa080-f12f-11ea-8c99-74f897e4c4eb.PNG)

<br>

## Development Environment

### Hardware Composition

![1](https://user-images.githubusercontent.com/50494545/92564579-5a39e480-f2b4-11ea-931b-cab9241d0d2c.PNG)

<br>

### Software Composition

![2](https://user-images.githubusercontent.com/50494545/92564612-67ef6a00-f2b4-11ea-944a-84718bbb02a9.PNG)

<br>

## Usage
+ 유튜브 사용 설명 링크

[![Watch the video](https://img.youtube.com/vi/oLQpSs1fuAk/2.jpg)](https://youtu.be/oLQpSs1fuAk)
