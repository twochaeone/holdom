![image](https://github.com/user-attachments/assets/ec6e8542-1280-451f-a39f-1d14fa5c44e3)# 🃏 텍사스 홀덤 웹 게임 

**순수 HTML과 JavaScript만으로 구현한 브라우저 기반 텍사스 홀덤 게임**입니다.  
카드 셔플, 딜링, 핸드 평가 로직, 턴 진행 등을 직접 구현하여 프론트엔드 로직의 구조화와 상태 관리 능력을 기를 수 있었습니다.


## 📌 주요 기능

- 1:1 텍사스 홀덤 게임 (플레이어 vs 시스템)
- 기본 게임머니: 1,000 (양측 동일)
- 프리플롭 자동 진행: 시스템이 선 베팅(10), 플레이어가 응답
- 커뮤니티 카드 오픈: 플롭 → 턴 → 리버 순
- 턴별 액션:
  - 플레이어가 먼저: 체크 / 콜 / 올인 선택
  - 시스템이 응답: 체크 / 콜 / 올인 로직 포함
- 핸드 평가 후 승자 결정 및 머니 배분
- 한쪽이 머니 0이 되면 게임 종료

## 🎲 게임 규칙 및 흐름

- 플레이어와 시스템이 1대1로 대결하는 구조입니다.
- 양쪽 모두 게임 시작 시 1,000의 머니를 보유합니다.
- **프리플롭**: 시스템이 먼저 10을 베팅 → 플레이어가 콜/폴드/올인 중 선택
- 이후 **플롭 → 턴 → 리버** 순으로 커뮤니티 카드가 오픈됩니다.
- 각 단계에서 플레이어가 먼저 행동하고, 시스템이 응답하는 방식입니다.
- 시스템의 모든 플레이는 랜덤으로 진행됩니다.
- 승자는 핸드 평가(페어, 스트레이트 등)로 결정되며, 이긴 쪽이 팟을 가져갑니다.
- 한 쪽의 돈이 모두 소진되면 게임은 종료됩니다.


### 1. 🟡 프리플롭 (Pre-Flop)

- **시작 머니**: 플레이어와 시스템은 각각 1,000의 게임머니를 가짐
- **선 베팅**: 시스템이 먼저 10을 베팅
![Image](https://github.com/user-attachments/assets/56f134b8-9061-4b21-b796-fe1f218d7e76)
- **플레이어 선택**: 콜(Call), 폴드(Fold), 올인(All-in) 중 선택 (예시 : 콜 선택)
- 다음 단계로 진행
![Image](https://github.com/user-attachments/assets/deb27145-41be-4705-9fa3-86adaaea7086)
 
### 2. 🟢 플롭 (Flop)

- **커뮤니티 카드 3장 공개**
- **플레이어 선 행동**: 체크(Check), 베팅(bet) 중 하나 선택
- 체크 선택시 시스템 베팅, 베팅 선택시 플레이어가 베팅 (예시 : 베팅 선택)
  ![Image](https://github.com/user-attachments/assets/5fa62439-162e-4c88-b140-66890764ee92)
- 폴드(fold),레이즈(raise), 콜 (call) 중 하나 선택 (예시 : 레이즈 선택)
  ![Image](https://github.com/user-attachments/assets/66e9541a-11e2-43cb-820d-6b78ed686019)
- 하프, 더블, 올인 중 하나 선택 (예시 : 사용자 하프 선택)
- **하프** : 현재 베팅금액(bet)의 1.5배를 베팅
- **더블** : 현재 베팅금액의  2배를 베팅, bet이 2배 증가
- **올인** : 가진 돈을 전부 베팅 
  ![Image](https://github.com/user-attachments/assets/6bf399af-096b-4f5d-b732-99e6a027b9a3)
  ![Image](https://github.com/user-attachments/assets/7692973c-aba8-4c77-950c-8e770faa864f)
- **시스템 응답**: 체크 / 콜 / 올인 중 랜덤으로 선택
  ![Image](https://github.com/user-attachments/assets/3b68eceb-6c70-4eae-9b67-5575d146208a)
  ![Image](https://github.com/user-attachments/assets/c916abce-f4a0-4824-9ecb-0738453ad18c)
  ![Image](https://github.com/user-attachments/assets/9bd01f2f-9e34-4731-bcac-7482b6529595)
  
- 베팅이 맞춰지면 다음 단계로 진행

### 3. 🔵 턴 (Turn)

- **커뮤니티 카드 1장 추가 공개**
- **행동 반복**: 시스템 -> 플레이어 순서로 위와 같은 선택 반복
  ![Image](https://github.com/user-attachments/assets/51f18ebc-b990-4d71-b169-d57658e17731)
  ![Image](https://github.com/user-attachments/assets/b61863b4-06be-4e66-8616-02a2b7e8a558)
  ![Image](https://github.com/user-attachments/assets/ecfb22e4-b754-4f5e-839f-ce587398177b)
  ![Image](https://github.com/user-attachments/assets/f7d4dfe2-1692-4558-95b7-8deab7b92fd3)
  ![Image](https://github.com/user-attachments/assets/e02c3ee3-11c7-4698-9c12-03d19334f886)
- 폴드 선택시 베팅 없음
 ![Image](https://github.com/user-attachments/assets/3fe1a7b7-e15d-4229-8caa-870896d6e922)
---

