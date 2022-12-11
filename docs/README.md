# 기능목록

## 입력을 담당하는 클래스 ClassName : InputView
- [ ] 메인 기능 입력받기
- [ ] 과정, 레벨, 미션 입력받기
- [ ] 재매칭 여부 입력받기
---
## 출력을 담당하는 클래스 ClassName : OutputView
- [ ] 매칭 결과 출력 - #printMatcingResult()
- [ ] 메인 화면 출력 - #printMain()
- [ ] 매칭 조건 입력창 출력 - #printMatchingDetails()
- [ ] 재매칭 여부 화면 출력 - #askReMatching()
- [ ] 초기화 문구 출력 - #printInitMessage()
---
## 페어를 매칭한다 domain : Pair
- 멤버 : List<List<String>> names, Part part, Mission
- ### Controller : PairMatchingController
- ### Service : PairMatchingService
  - [ ] 페어 매칭 기능 - #createPairs()
  - [ ] 페어 조회 기능 - #findPair()
  - [ ] 페어 초기화 기능 - #initPair()
- ### Repository : PairMatchingRepository
  - [ ] 미션으로 매칭된 페어들 조회 - #getPairByMission()
  - [ ] 생성된 페어들 저장 - #save()
  - [ ] 페어 전체 삭제 - #deleteAll()
---
## 미션 매칭한 후 매칭된 미션을 저장 domain : Mission
- [ ] 미션의 이름을 받아오는 기능 - #getName()
- ### Service : MissionService
  - [ ] 미션 매칭 - #createMission()
  - [ ] 매칭된 미션 전체 삭제 - #deleteAll()
  - [ ] 미션의 레벨로 매칭된 미션들 조회 - #getMissionsByLevel()
  - [ ] 미션의 이름으로 매칭된 미션 조회 - #getByName()
- ### Repository : MissionRepository
  - [ ] 미션 저장 - #save()
  - [ ] 매칭된 미션 전체 삭제 - #deleteAll()
  - [ ] 미션의 레벨로 매칭된 미션들 조회 - #findAllByLevel()
  - [ ] 미션의 이름으로 매칭된 미션 조회 - #findByName()
---
## 프론트엔드 크루들의 이름을 저장하는 일급컬렉션 ClassName : FrontMembers
- [ ] 프론트엔드 크루원들의 이름 받아오기 - getFrontNames()
---
## 백엔드 크루들의 이름을 저장하는 일급컬렉션 ClassName : BackMembers
- [ ] 백엔드 크루원들의 이름 받아오기 - getBackNames()
---
## 파일을 읽어들이는 클래스 ClassName : FileReader
- [ ] `backend-crew.md` 를 읽어들이는 기능 - #readBackCrew()
- [ ] `frontend-crew.md` 를 읽어들이는 기능 - #readFrontCrew()

## 메인 기능 enum Name : Main
- MATCHING, SEARCHING, INIT, QUIT
## 미션 레벨 enum Name : Level
- ONE,TWO,THREE,FOUR,FIVE
## 파트 enum : Part
- FRONT_END , BACK_END