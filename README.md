# Tadak
------------
### Introduction<br />
* #### '쓰면 외워진다!'
저희 "타닥" 프로젝트는 개인 프로젝트로 타자게임과 광고를 결합시키는 의도로 진행되는 랭킹제 타자게임 어플입니다.  "타닥"은 Swift로 작성되었습니다. 또한 랭킹제를 도입하기 위해 Firebase를 이용해 전화인증 회원가입제로 운영됩니다. <br />

* #### 실시간으로 전체 회원중에 자신이 몇등인지를 알려주는 랭킹제
랭킹은 **DB를 점수별 노드로 나누어 점수구간별로 인원을 더해서 자신보다 높은 순위의 사람들의 수를 구하는 방식을 택하여 비용과 속도 측면에서 효율성을 늘렸습니다.** 그리고 적당한 DB의 크기를 위해 개인 게임 기록들은 모두 30일이 지나면 사라집니다.(물론 자신의 최고기록은 시간에 관계없이 계속 유지됩니다.) 
* #### "타닥"은 오로지 빠르게 치는 것에만 집중한다는 것입니다.
"타닥"이라는 타자게임은 타수를 계산하지 않습니다. 속도와 정확성은 모두 시간에 반영되게 설계되어 있습니다. 실시간으로 자모음을 분리해 자신의 오타갯수를 파악합니다. 그 후 그 갯수에 비례하게 시간을 늘립니다. 즉 엉뚱하게 친다면 시간은 계속 늘어나고 100초를 넘어가면 탈락입니다. 이러한 타닥의 특성으로 광고와 보상을 같이 연결하여 사람들의 참여를 유도할 수 있습니다. <br />

email 주소 : tlsgyrms123@gmail.com / freedeveloper97@gmail.com<br />
blog 주소 : https://shinhyogeun.tistory.com / https://fdee.tistory.com<br />

### 자세한 특징
------------
1. 타자게임을 회원제(전화인증)로 운영합니다.
2. 타닥은 오로지 시간을 기준으로 랭킹을 만듭니다.(오타갯수를 실시간으로 파악하여 자동으로 시간이 늘어나거나 오타를 수정하면 다시 줄어들게 구성되어 있습니다.)
3. 타닥의 게임내용, 회원정보, 랭킹정보는 Firebase와 연동되어 있습니다.
4. firebase Realtime Database를 이용한 전체 이용자 중 자신의 순위를 실시간으로 파악할 수 있게합니다.

### Development Environment
------------
- Xcode
- Firebase
- Xd

### Refactoring
---------------
- ( 1 )  로그인이 되어있는지 확인한다.
    <br>
    <br>
    <strong>로그인이 되어있을 때</strong><br>
    - 바로 메인화면으로 들어간다.
    
    
    <strong>로그인이 되어있지 않았을 때</strong><br>
    - 휴대폰 번호를 입력받는다.
    - 인증번호를 보낸다.(**반드시 다시 휴대폰 번호를 입력할 방법을 제공해야 한다.**)
    - 검증후 메인화면으로 들어간다.

    
    - ( 2 ) 게임 실행 과정
        <br>
        <br>
        <strong>1. 게임 선택화면</strong><br>
            - 게임을 선택할 수 있는 화면을 보여준다.
            - 게임 안의 게임 목록을 불러와 다음 화면을 보여준다.

 
