# Kartrider_Riderinfo_Crawling

- [카트라이더 공식웹 차고 페이지](https://kart.nexon.com/Garage/Main?strRiderID=InsanePhin) 크롤링

디스코드 `연습카트`봇에 사용되었으며 서비스 종료로 인해 오픈소스로 전환하였습니다.

### 시작하게된 동기

> 카트를 즐기다가 카트 전적이나 기타 정보를 알 수 있는 디스코드 봇이 보이지 않아 코딩을 배워볼 겸 처음 시작한 프로젝트이며,
이 프로젝트를 시작으로 파이썬에 처음 접하게 되었고 푹 빠지게 되었습니다.

### 주의사항

> 해당 코드는 `파이썬을 처음 접하고 작성한 코드`이며,
`requests`모듈을 사용하여 동기함수만 지원합니다. 
크롤링 속도를 개선하기위해 `aiohttp`를 사용하여 비동기함수를 지원할 예정입니다.

### 작동 원리

1. 라이더명 입력
2. 카트라이더 공식 api를 통해 정확한 라이더명 get
3. https://kart.nexon.com/Garage/(Main/Record/Item/Emblem)?strRiderID=라이더명 크롤링

### 출력 예시

```sh
$ python garage.py
라이더명을 입력해주세요 : insanephin

라이더명 - InsanePhin
클럽명 - Elyou
TMI 바로가기 - https://tmi.nexon.com/kart/user?nick=InsanePhin
라이더생성일 - 2017-03-01 (1520일 동안)
총 주행시간 - 44286분
마지막 접속일 - 2021-04-30
종합승률 - 43%
스피드전승률 - 36%
아이템전승률 - 37%
레벨이미지(글러브) - https://ssl.nx.com/s2/game/kart/kart/hands/hand_106_23.gif
라이더이미지 - https://avatarimg.kart.nexon.com/2019/525/058/1695058525.png
```