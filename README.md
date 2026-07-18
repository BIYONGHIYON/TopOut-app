<div align="center">
  <img width="180" height="180" alt="TopOut logo" src="https://github.com/user-attachments/assets/f3f75e67-414c-4a6a-92f2-52b47f9badbd" />

# TopOut

**등반 시작부터 완등 순간까지, 필요한 구간을 자동으로 찾아주는 클라이밍 촬영 앱**

iOS · Android

<sub>현재 개발 버전: 1.2</sub>

</div>

---

## 소개

**TopOut**은 실내 클라이머가 긴 촬영 영상에서 실제 등반 구간을 더 빠르게 찾고 저장할 수 있도록 돕는 모바일 앱입니다.

사용자가 촬영 구도와 매트 경계선을 설정하면, 앱이 매트 주변의 영상 변화와 사람의 자세를 단계적으로 분석해 등반 시작과 종료 후보 시점을 찾습니다.

탑홀드 선택 기능을 사용하는 경우에는 사용자가 지정한 홀드와 신체 관절이 가장 가까워진 순간을 기준으로 종료 후보 시점을 계산합니다. 탑홀드를 선택하지 않은 경우에는 자세 분석 과정에서 신체가 가장 높은 위치에 도달한 순간을 종료 후보로 활용합니다.

정상적인 촬영 상황에서는 사용자가 직접 녹화를 종료할 때까지 영상이 계속 기록되며, 한 번의 연속 촬영 안에서 여러 번의 등반 시도를 각각 감지할 수 있습니다.

촬영이 끝나면 감지된 구간을 확인하고, 시작점과 종료점을 직접 미세 조정한 뒤 원하는 부분만 기기의 사진 또는 동영상 보관함에 저장할 수 있습니다.

## 주요 기능

* **매트 경계선 탐지 및 수동 보정**
  벽과 매트의 경계를 자동으로 찾고, 필요한 경우 사용자가 직접 경계선의 위치를 조정할 수 있습니다.

* **3프레임 간격의 움직임 감지**
  촬영 시작 화면과 계속 비교하지 않고, 현재 분석 프레임을 3개 분석 프레임 전과 비교합니다. 촬영 시작 시 이미 존재하던 고정 노이즈나 조명 차이로 인해 자세 분석이 불필요하게 계속 실행되는 현상을 줄입니다.

* **Motion Detection → Pose Detection 단계형 분석**
  매트 경계 주변의 영상 변화를 먼저 가볍게 확인한 뒤, 실제 움직임 후보가 감지된 경우에만 자세 분석을 실행합니다.

* **플랫폼별 온디바이스 자세 분석**
  iOS에서는 Apple Vision Human Body Pose를 사용하고, Android에서는 TensorFlow Lite 기반 MoveNet SinglePose Lightning FP16 모델을 사용합니다.

* **Android 스마트 크롭 추적**
  Android에서는 사람 크기에 비례한 관절 움직임이 일정 시간 확인된 경우에만 MoveNet 스마트 크롭을 활성화해 정적인 클라이밍 홀드가 사람으로 오인되는 문제를 줄입니다.

* **MobileSAM 기반 탑홀드 선택**
  목표 홀드를 화면에서 탭해 선택할 수 있으며, 선택된 홀드 영역을 마스크 형태로 화면에 표시합니다.

* **자동 등반 구간 감지**
  매트 경계 통과, 사람 자세, 관절 위치 변화를 바탕으로 등반 시작과 종료 후보 시점을 계산합니다.

* **다중 시도 감지**
  하나의 연속 녹화 안에서 여러 번의 등반 시도를 각각 구분해 기록합니다.

* **자동 선택 및 정밀 트리밍**
  감지된 등반 구간을 자동으로 제안하고, 사용자가 시작점과 종료점을 직접 세밀하게 조정할 수 있습니다.

* **선택 구간만 저장**
  전체 촬영 영상에서 사용자가 선택한 구간만 편집해 기기의 사진 또는 동영상 보관함으로 내보냅니다.

* **안전한 녹화 종료**
  앱의 백그라운드 진입, 카메라·마이크 중단, 저장공간 부족 등의 상황이 발생하면 현재까지 촬영된 영상 파일을 안전하게 마무리합니다.

## 작동 흐름

1. 촬영 해상도, 프레임률, 화면 비율 등의 기본 설정을 선택합니다.
2. 벽, 매트, 클라이머가 모두 보이도록 카메라 구도를 맞춥니다.
3. 자동으로 감지된 매트 경계선을 확인하고 필요한 경우 직접 보정합니다.
4. 탑홀드 선택 기능을 사용하는 경우 완등 목표 홀드를 지정합니다.
5. 녹화를 시작하면 앱이 현재 프레임과 3개 분석 프레임 전을 비교해 매트 주변의 변화를 감지합니다.
6. 움직임 후보가 확인되면 기기 내 자세 분석을 실행해 사람과 등반 시작 여부를 확인합니다.
7. 등반 중에는 자세와 관절 위치를 분석해 종료 후보 순간을 기록합니다.
8. 한 번의 촬영에서 여러 시도가 발생하면 각 등반 구간을 별도로 저장합니다.
9. 녹화 종료 후 자동으로 제안된 구간을 확인하고 시작점과 종료점을 직접 조정합니다.
10. 원하는 구간만 기기의 사진 또는 동영상 보관함에 저장합니다.

## 플랫폼별 구현

| 구분        | iOS                          | Android                           |
| --------- | ---------------------------- | --------------------------------- |
| 현재 버전     | 1.2                          | 1.2                               |
| UI        | UIKit                        | Jetpack Compose                   |
| 카메라·녹화    | AVFoundation                 | CameraX                           |
| 매트 경계 탐지  | 자체 영상 처리                     | 자체 영상 처리                          |
| 움직임 비교    | 현재 프레임 ↔ 3개 분석 프레임 전         | 현재 프레임 ↔ 3개 분석 프레임 전              |
| 자세 분석     | Apple Vision Human Body Pose | MoveNet SinglePose Lightning FP16 |
| 자세 분석 런타임 | Vision                       | TensorFlow Lite                   |
| 탑홀드 분할    | Core ML MobileSAM            | ONNX Runtime MobileSAM            |
| 영상 재생·편집  | AVFoundation                 | AndroidX Media3                   |
| 결과 영상 저장  | Photos                       | MediaStore                        |

## 분석 구조

```text
매트 경계 주변 CV 변화 감지
        ↓
현재 프레임과 3개 분석 프레임 전 비교
        ↓
움직임 후보 확인
        ↓
기기 내 사람 자세 분석
        ↓
매트 경계 통과 여부 확인
        ↓
등반 시작 구간 기록
        ↓
탑홀드 근접 또는 최고 도달 순간 계산
        ↓
종료 후보 구간 기록
        ↓
사용자 검토 및 정밀 트리밍
```

영상 분석은 실시간 녹화 영상에서 수행되지만, 감지 결과는 최종 판단이 아닌 **편집 후보 구간을 제안하기 위한 보조 정보**로 사용됩니다. 사용자는 결과 화면에서 시작점과 종료점을 직접 변경할 수 있습니다.

## 개인정보 및 영상 처리

* TopOut은 회원가입 없이 사용할 수 있습니다.
* 이름, 이메일 주소, 위치정보, 기기 식별자 등의 개인정보를 수집하지 않습니다.
* 촬영한 원본 영상과 분석용 이미지 프레임을 TopOut 개발자 서버로 업로드하지 않습니다.
* 움직임 감지, 자세 추정, 탑홀드 분할 등의 영상 분석은 사용자의 기기 내에서 수행됩니다.
* 사용자가 저장을 선택한 결과 영상만 기기의 사진 또는 동영상 보관함으로 내보냅니다.
* 현재 버전에는 광고 및 외부 사용자 행동 분석 도구가 포함되어 있지 않습니다.

자세한 내용은 아래 개인정보 처리방침에서 확인할 수 있습니다.

[TopOut 개인정보 처리방침](https://topoutprivacy.vercel.app/)

## 출시 상태

* **App Store:** [버전 1.2 출시](https://apps.apple.com/kr/app/topout/id6790163178)
* **Google Play:** 버전 1.2 출시 준비 중

스토어 등록이 완료되면 이 문서에 각 플랫폼의 다운로드 링크를 추가할 예정입니다.

## 지원 및 문의

사용 중 문제가 발생하거나 개선 의견이 있다면 아래 지원 페이지를 이용해 주세요.

* [문제 신고 및 기능 제안](https://biyonghiyon.github.io/TopOut-app/)

문제를 등록할 때 다음 정보를 함께 적어주면 확인에 도움이 됩니다.

* 사용 기기 모델
* 운영체제 및 버전
* TopOut 앱 버전
* 문제가 발생한 화면
* 문제 재현 순서
* 오류 화면 또는 로그 스크린샷

개인정보 처리 및 기타 문의:

* **개발자·운영자:** 이병현 (BIYONGHIYON)
* **이메일:** [byeonghyeon383@gmail.com](mailto:byeonghyeon383@gmail.com)

## 저장소 안내

이 저장소는 TopOut의 **공개 소개, 지원, 개인정보 처리방침 및 업데이트 안내**를 위한 저장소입니다.

실제 App Store 및 Google Play 배포용 애플리케이션 소스 코드는 별도의 비공개 저장소에서 관리합니다.

## 기술 구성

### iOS

* Swift
* UIKit
* AVFoundation
* Vision
* Core ML
* Photos
* MobileSAM

### Android

* Kotlin
* Jetpack Compose
* CameraX
* TensorFlow Lite
* MoveNet SinglePose Lightning FP16
* ONNX Runtime
* AndroidX Media3
* MediaStore
* MobileSAM

### Computer Vision

* Mat Boundary Detection
* Rolling Frame Difference
* Motion Detection
* Human Body Pose Estimation
* Smart Crop Pose Tracking
* MobileSAM Image Segmentation

### Video

* Continuous Video Recording
* Multiple Climb Attempt Detection
* Automatic Segment Selection
* Precision Trimming
* Selected Range Export
* Background and Low-Storage Safe Finalization

---

<div align="center">
  <strong>TopOut</strong><br />
  등반 기록에 필요한 장면만 더 빠르게.
</div>
