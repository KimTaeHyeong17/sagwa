---
description: 제스처 인식기에서 앱의 이벤트 처리 로직을 캡슐화하여 앱 전체에서 해당 코드를 재사용 할 수 있습니다.
---

# 터치, 누르기, 제스처

> 원문 출처  
> [https://developer.apple.com/documentation/uikit/touches\_presses\_and\_gestures](https://developer.apple.com/documentation/uikit/touches_presses_and_gestures)

## 개요

표준 UIKit 뷰 및 컨트롤을 사용하여 앱을 작성하는 경우 UIKit은 자동으로 터치 이벤트\(멀티터치 이벤트 포함\)를 처리합니다. 그러나 커스텀 뷰를 사용하여 내용을 표시하는 경우 뷰에서 발생하는 모든 터치 이벤트를 처리해야 합니다. 터치 이벤트를 직접 처리하는 방법은 두 가지가 있습니다.

* 제스처 인식기를 사용하여 터치를 추적합니다. [UIKit 제스처 처리](handling_uikit_gestures.md)를 참조하세요.
* [UIView](../views_and_controls/uiview.md) 하위 클래스에서 직접 터치를 추적합니다. [뷰에서 터치 처리하기](../../../etc/not-found.md)를 참조하세요.

## 주제

### 첫 번째 단계

* 응답자\(Responder\)와 응답자 체인을 통한 이벤트 처리 이벤트가 앱을 통해 전파되는 방법과 이를 처리하는 방법에 대해 알아봅니다.
* _class_ [UIResponder](uiresponder.md) 이벤트에 응답하고 이벤트를 처리하기 위한 추상 인터페이스
* _class_ UIEvent 사용자와의 단일한 상호 작용을 설명하는 객체

### 터치

* 뷰에서 터치 처리하기

  터치 핸들링이 뷰 시각화와 복잡하게 연결되어 있다면 뷰 서브 클래스에서 직접 터치 이벤트를 사용하세요.

* 애플 펜슬 입력 처리하기 애플 펜슬의 터치를 감지하고 응답하는 방법에 대해 알아보세요.
* 3D 터치 이벤트의 압력 추적

  터치의 강도에 따라서 컨텐츠를 조작하세요.

* 터치 입력의 힘, 고도, 방위 속성 나타내기 애플 펜슬과 터치 입력을 뷰에서 잡아냅니다.
* 그리기 앱에서 터치 입력 이용하기 터치를 일련의 획으로 캡처하여 드로잉 캔버스에서 효율적으로 렌더링합니다.
* _class_ UITouch 화면에서 발생하는 터치의 위치, 크기, 움직임과 압력을 나타내는 객체

### 버튼 누르기

* _class_ UIPress 특정 이벤트에 대해 화면에 발생하는 터치와 움직임을 나타내는 객체
* _class_ UIPressesEvent 연결된 원격 또는 게임 컨트롤러처럼 장치에서 사용할 수 있는 물리적 버튼들의 상태를 나타내는 이벤트입니다.

### 표준 제스처

* [UIKit 제스처 처리](handling_uikit_gestures.md) 제스처 인식기를 사용하여 터치 처리를 단순화하고 일관적인 사용자 환경을 만드세요.
* [다중 제스처 인식기 조정](coordinating-multiple-gesture-recognizers.md) 동일한 view 내에서 여러 제스처 인식기를 사용하는 방법을 알아보세요.
* _class_ UIHoverGestureRecognizer 뷰에서 포인터 움직임을 잡아내는 제스처 인식기
* _class_ [UILongPressGestureRecognizer](uilongpressgesturerecognizer.md) 길게 누르기 제스처를 인식하는 [UIGestureRecognizer](uigesturerecognizer.md)의 하위 구상 클래스
* _class_ [UIPanGestureRecognizer](uipangesturerecognizer/) 드래그 제스처를 인식하는 [UIGestureRecognizer](uigesturerecognizer.md)의 하위 구상 클래스
* _class_ UIPinchGestureRecognizer pinching 제스처를 인식하는 [UIGestureRecognizer](uigesturerecognizer.md)의 하위 구상 클래스
* _class_ UIRotationGestureRecognizer 두 개의 터치로 회전하는 제스처를 인식하는 [UIGestureRecognizer](uigesturerecognizer.md)의 하위 구상 클래스
* _class_ UIScreenEdgePanGestureRecognizer 스크린 가장자리로부터의 드래그 제스처를 인식하는 [UIGestureRecognizer](uigesturerecognizer.md)의 하위 구상 클래스
* _class_ UISwipeGestureRecognizer 하나 이상의 방향으로 스와이프하는 제스처를 인식하는 [UIGestureRecognizer](uigesturerecognizer.md)의 하위 구상 클래스
* _class_ UITapGestureRecognizer 하나 또는 다중 탭 동작을 인식하는 [UIGestureRecognizer](uigesturerecognizer.md)의 하위 구상 클래스

### 커스텀 제스처

* Implementing a Custom Gesture Recognizer 언제, 그리고 어떻게 제스처 인식기를 직접 빌드할 수 있는지 알아보세요.
* _class_ [UIGestureRecognizer](uigesturerecognizer.md) 구상 제스처 인식기의 기본 클래스
* _protocol_ UIGestureRecognizerDelegate 제스처 인식기의 위임자에 의해서 구현되는 메서드들. 앱의 제스처 인식 동작을 정밀하게 조정합니다.

### 3D 터치 상호작용

* class UIPreviewInteraction 3D 터치에 대한 응답으로 커스텀 UX를 제공하기 위해 뷰를 등록하는 클래스
* protocol UIPreviewInteractionDelegate 프리뷰 상호 작용의 진행 상황을 알리는 메서드 셋
* protocol UIPreviewActionItem 이 메서드 집합은 Peek 액션과 Peek 액션 그룹에 적용할 수 있는 스타일을 정의하고 peek 액션의 사용자가 볼 수 있는 제목에 대한 읽기 전용 접근자를 정의합니다.

## 같이 보기

### 유저 상호작용

* 드래그 앤 드롭 View와 상호작용 API를 사용해서 앱에서 드래그 앤 드롭 기능을 사용하세요.
* 펜슬 상호작용 애플 펜슬의 더블 탭 동작을 처리하세요.
* 포커스 기반 네비게이션

   원격 또는 게임 컨트롤러를 사용해서 UIKit 앱 인터페이스를 탐색합니다.

* 메뉴와 단축키 메뉴 시스템, 컨텍스트 메뉴, 홈 화면 퀵 액션과 키보드 단축키를 이용하여 앱의 상호작용을 단순화하세요.
* 접근성 도구 장애인을 포함한 모든 사용자가 앱에 접근하도록 만드세요.

