---
description: UIKit 앱의 View 계층구조를 관리하는 객체
---

# UIViewController

## 개요

UIViewController 클래스는 모든 view controller에 공통적인 동작을 정의합니다.  
UIViewController 클래스의 인스턴스를 직접 만드는 경우는 거의 없습니다. 대신 UIViewController를 하위 클래스로 만들고 view controller의 뷰 계층 구조를 관리하는 데 필요한 메서드와 속성을 추가하세요.

view controller의 주요 임무는 다음과 같습니다.

* 데이터 변화에 따라서 view 컨텐츠를 업데이트
* view와의 사용자 상호작용에 응답
* view를 리사이징하고 전체적인 인터페이스의 레이아웃 관리
* 앱 내에서 \(다른 view controller를 포함한\) 다른 객체와의 조정

view controller는 자신이 관리하는 view에 단단히 바인딩되어 있고 view 계층에서 이벤트를 처리하는 데 참여합니다. 특히 view controller는 UIResponder 객체로써 view controller의 루트 뷰와 해당 뷰의 상위 뷰 사이에 있는 responder chain에 삽입되며 일반적으로 다른 view controller에 속합니다. view controller상의 어떤 view도 이벤트를 처리하지 않는다면 view controller는 직접 이벤트를 처리하거나 상위 뷰로 전달할 수 있는 옵션을 제공합니다.

view controller는 단독적으로 사용되는 일이 거의 없습니다. 대부분의 경우 유저 인터페이스의 일부를 담당하는 여러개의 view controller가 같이 사용됩니다. 예를 들어, 하나의 view controller에 항목 테이블이 표시되는 동안 다른 view controller에 해당 테이블에서 선택한 항목이 표시됩니다.  
일반적으로 하나의 view controller에는 하나의 뷰만 표시됩니다. view controller는 새로운 뷰 세트를 표시하기 위해 다른 view controller를 표시하거나, 다른 view controller의 컨텐츠에 대한 컨테이너 역할을 하고 원하는 대로 뷰를 애니메이션할 수 있습니다.

## SubClassing Notes



### 뷰 관리



## 뷰 관련 Notification 처리



## 뷰 회전 처리



### 컨테이너 뷰 컨트롤러 구현



### 메모리 관리



### 상태 보존과 복구



## 주제

### 프로그래밍적으로 View Controller 생성하기



### 스토리보드와 Segue로 상호작용



### View 관리



### View Controller 표시하기



### 커스텀 화면 전환과 프레젠테이션



### View 이벤트에 응답하기



### View Safe Area 확장



### View Magin 관리하기



### View 레이아웃 동작 설정



### View 회전 설정



### 환경 변화에 적응하기



### 인터페이스 스타일 조정



### 커스텀 컨테이너 내의 하위 View Controller 관리



### 컨테이너에 포함하는 이벤트에 응답



### 연관된 다른 View Controller 얻기



### 메모리 경고 처리



### 상태 복구 관리



### 앱 확장 지원



### 3D터치 미리보기, 미리보기 퀵 액션과 작업하기



### 시스템 제스처 인식기로 조정



### 상태바 관리



### 제스처 설정



### 네비게이션 인터페이스 설정



### 탭바 아이템 설정



### 뷰 컨트롤러에 에디팅 동작 추가하기



### 사용가능한 키 커맨드에 접근



### Nib 파일 정보 얻기



### 상수Constants



### 알림Notification



### 지원중단Deprecated



## 연관 문서

### 상속받은 상위 클래스



### 준수하는 프로토콜

### 
