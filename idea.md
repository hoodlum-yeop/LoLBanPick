포지션을 1(top),2(jungle),3(mid),4(bot),5(support)
=> 숫자를 이용하지 않고 lambda로 구현

소환사와 챔피언 클래스를 **interface**로 동시에 구현

챔피언 클래스
- 사용가능 여부(픽이나 벤이되면 거짓으로 만들어주면 됨)
- 챔피언 이름
- 포지션(포지션에 맞는 것만 사용가능)

소환사 클래스
- 레벨
- 픽순서
- 포지션
- 소환사 이름
- 소속 팀

클라이언트
- 벤 리스트
- 픽리스트
- 소환사리스트 (색깔별로 존재) (소환사 픽순서 및 포지션 순서 정렬 가능해야함)
```
    blue        |       purple
ban  lulu,      |       ryze
1st             |
2nd             | 
3rd             |
4th             |
5th             |
--ban phaze--
plz enter champion (enter 'list' if you wanna see champion list)
ryze, lulu, maokai,
: 
```

**list 입력시 모든 챔피언 출력**
- 구현은 man 페이지처럼 

폰트는 나중에 결정

우리가 블루팀이라 가정 -> purple은 랜덤으로 진행 (총 입력은 8개)

순서
1. 위 배경 출력(이하 픽창)
2. 벤 타이핑으로 함(단, 불가능한 것을 진행시 경고 및 재 실행)(시간 제한 초과시 랜덤)
3. 3가지 벤 완료시 픽으로 (같은 진행)
4. 픽완료시 순서를 라인별로 정리함

```
    blue        |       purple
top             |
jun             | 
mid             |
bot             |
sup             |

--game start--
```
