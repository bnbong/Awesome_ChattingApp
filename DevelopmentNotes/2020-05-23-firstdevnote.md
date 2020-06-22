## 1st Development Note

안녕하십니까, 한양대 ERICA 오픈소스sw TEAM 두둥등장(김택윤,남현기,박종윤,이준혁)입니다.

저희팀은 이번 오픈소스sw 기말프로젝트 결과물로 한양대학교에서 온라인 수업이나 과제 등을 확인할 때 사용하는 블랙보드의 API를 통해,
블랙보드를 사용하는 한양대학교 학생이 수강하는 수업의 과제 마감일, 온라인 강의 마감일이나 공지사항을 확인할 수 있게 해주는 캘린더 역할을
겸할 수 있는 채팅앱을 개발하기로 결정했습니다.

팀을 구성한 후 진행한 첫 회의에서는 저희 팀이 개발해 나갈 앱의 대략적인 기능과 간단한 UI 디자인을 진행했습니다.
(아래는 최종 아이디어들을 결합한 결과물의 스케치 사진입니다.)

![1stpicture](docs/1stday.png)
사진이 나오지 않는 경우, [1stday](https://github.com/bnbong/awesomechatappdev/blob/master/docs/1stday.png)에서 확인하세요.

약 3시간 정도 회의한 결과, 저희 팀이 제작할 앱에서는 해당 학생의 블랙보드와의 계정연동 및 채팅기능 사용을 위한 블랙보드에 저장되어 있는
아이디의 로그인 기능과 해당 앱을 사용중인 모든 학생들과 소통이 가능한 채팅창을 제공하는 기능, 블랙보드에 로그인한 회원정보를 바탕으로
학생이 현재 수강하고 있는 과목들의 공지사항, 아직 미수강한 온라인 강의의 마감기한, 과제의 마감기한과 시간표를 알려주는 기능을 포함시키기로 결정했습니다.

회의를 진행하면서 많은 의견이 오고 갔습니다. 로그인을 하는 서비스에서 앱의 사용자가 입력을 해야할 회원정보가 블랙보드의 회원정보만을 입력하게 하자고 하는 의견과, 채팅앱과 블랙보드 회원정보를 따로 나누어 2번의 로그인을 실시하게끔 하자고 하는 의견의 충돌도 있었습니다. 계속된 회의 끝에 회원정보는
블랙보드의 회원정보 하나만을 입력하게 하는 방식으로 결정하였습니다.

블랙보드의 API를 따오기 위해 연구하던 도중, 저희는 그동안 잘 몰랐던 블랙보드 웹에서 이미 제공해주던 마감기한이 존재하는 과제들을 한눈에 볼 수 있는
캘린더 형식의 뷰어와 그동안 해결했던 과제들의 점수를 한 화면에 볼 수 있는 기능을 발견했습니다. 이에 이미 블랙보드 웹에서 제공을 하는 서비스를 그대로 옮기는 것에 불과한 결과물을 만들까 두려웠으나, 해당 뷰어에는 온라인 영상의 마감기한을 알 수 있는 기능은 없었습니다. 즉, 온라인 영상물의 마감기한을 확인하려면 직접 그 수업칸에 들어가서 일일히 확인하는 방법밖에 없습니다. 때문에 저희는 온라인 영상의 마감기한 까지도 확인할 수 있게 해주는
서비스를 만들기로 하고, 이미 좋은 시간표 UI를 가지고 있는 앱인 '에브리타임'의 시간표를 저장하여 확인할 수 있게 해주는 서비스도 만들기로 결정했습니다.

회의에 마지막에서는 프로젝트의 결과물의 서비스를 구상한 후 다음 회의 진행때 까지 각자 블랙보드에서 API를 얻어오는 방법을 연구하기로 결정했습니다.
이에 참고가 될만한 오픈소스가 없나 찾아보다가 파이썬 기반으로 고려대학교의 블랙보드의 API를 따오는 오픈소스를 발견했습니다. 저희는 자바기반의
앱을 만들기로 결정했기 때문에 이 오픈소스를 공부하고, 이해하면서 파이썬이 아닌 자바로 이와 비슷한 메소드를 제작할 방법을 연구하기로 결정하면서 첫 번째 회의를 마쳤습니다.

2020/05/23