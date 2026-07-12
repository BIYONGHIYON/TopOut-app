<div align="center">
  <img width="180" height="180" alt="Default-logo" src="https://github.com/user-attachments/assets/f3f75e67-414c-4a6a-92f2-52b47f9badbd" />

  # TopOut

  **등반 시작부터 완등 순간까지, 자동으로 찾아주는 클라이밍 촬영 앱**

  iOS · Android
</div>

---

## 소개

**TopOut**은 실내 클라이머가 긴 촬영 영상에서 실제 등반 구간을 더 빠르게 찾고 저장할 수 있도록 돕는 모바일 앱입니다.

사용자가 촬영 구도와 매트 경계선을 설정하면, 앱이 매트 주변의 움직임과 사람의 자세를 분석해 등반 시작과 종료 후보 시점을 찾습니다. 탑홀드 선택 기능을 사용하는 경우에는 지정한 홀드에 가장 가까웠던 순간을 기준으로 자동 편집 구간을 제안합니다.

녹화는 사용자가 직접 종료할 때까지 계속되며, 한 번의 촬영 안에서 여러 번의 등반 시도를 감지할 수 있습니다. 촬영 후에는 자동 선택된 구간을 확인하고 시작점과 종료점을 직접 조정한 뒤 원하는 부분만 저장할 수 있습니다.

## 주요 기능

- **매트 경계선 탐지 및 수동 보정**  
  벽과 매트의 경계를 자동으로 찾고, 필요한 경우 사용자가 직접 조정할 수 있습니다.

- **Motion Detection → Pose Detection 단계형 분석**  
  가벼운 움직임 감지 후 필요한 순간에만 자세 분석을 실행해 불필요한 연산을 줄입니다.

- **MobileSAM 기반 탑홀드 선택**  
  목표 홀드를 탭해 선택하고, 선택된 영역을 화면에 표시합니다.

- **자동 등반 구간 감지**  
  매트 경계 통과와 자세 변화를 바탕으로 등반 시작 및 종료 후보 시점을 계산합니다.

- **다중 시도 감지**  
  하나의 연속 녹화 안에서 여러 번의 등반 시도를 각각 구분합니다.

- **자동 선택 및 정밀 트리밍**  
  감지된 구간을 자동으로 제안하고, 시작점과 종료점을 직접 미세 조정할 수 있습니다.

- **안전한 녹화 종료**  
  앱 백그라운드 진입, 촬영 중단, 저장공간 부족 등의 상황에서 영상 파일을 안전하게 마무리합니다.

## 작동 흐름

1. 촬영 해상도와 프레임 등 기본 설정을 선택합니다.
2. 벽, 매트, 클라이머가 모두 보이도록 카메라 구도를 맞춥니다.
3. 매트 경계선을 확인하고 필요하면 직접 보정합니다.
4. 선택 기능을 사용하는 경우 완등 목표 홀드를 지정합니다.
5. 녹화를 시작하면 앱이 매트 주변 움직임을 감지합니다.
6. 시작 후보가 확인되면 자세 분석을 통해 등반 구간을 기록합니다.
7. 녹화 종료 후 자동 선택된 구간을 확인하고 직접 조정합니다.
8. 원하는 구간만 기기의 사진 또는 동영상 보관함에 저장합니다.

## 플랫폼

| 구분 | iOS | Android |
|---|---|---|
| UI | UIKit | Jetpack Compose |
| 카메라 | AVFoundation | CameraX |
| 자세 분석 | Vision Human Body Pose | ML Kit Pose Detection |
| 탑홀드 분할 | Core ML MobileSAM | ONNX Runtime MobileSAM |
| 영상 편집·저장 | AVFoundation · Photos | Media3 · MediaStore |

## 개인정보 및 영상 처리

- TopOut은 회원가입 없이 사용할 수 있습니다.
- 촬영한 원본 영상과 분석용 이미지 프레임은 개발자 서버로 업로드하지 않습니다.
- 영상 및 이미지 분석은 기기 내에서 수행됩니다.
- 사용자가 저장을 선택한 결과 영상만 기기의 사진 또는 동영상 보관함에 저장됩니다.
- 현재 버전에는 광고가 포함되어 있지 않습니다.

자세한 내용은 추후 공개되는 개인정보처리방침에서 확인할 수 있습니다.

## 출시 상태

- App Store: 출시 준비 중
- Google Play: 출시 준비 중

스토어 등록이 완료되면 이 문서에 다운로드 링크를 추가할 예정입니다.

## 지원 및 문의

사용 중 문제가 발생하거나 개선 의견이 있다면 아래 GitHub Issues를 이용해 주세요.

- 문제 신고 및 기능 제안: [GitHub Issues](https://github.com/BIYONGHIYON/topout-app/issues)

문제를 등록할 때 다음 정보를 함께 적어주면 확인에 도움이 됩니다.

- 사용 기기와 운영체제 버전
- TopOut 앱 버전
- 문제가 발생한 화면과 재현 순서
- 오류 화면 또는 로그 스크린샷

## 저장소 안내

이 저장소는 TopOut의 **공개 소개, 지원, 업데이트 안내**를 위한 저장소입니다. 실제 배포용 애플리케이션 소스 코드는 별도의 비공개 저장소에서 관리합니다.

## 기술 구성

- iOS: Swift, UIKit, AVFoundation, Vision, Core ML
- Android: Kotlin, Jetpack Compose, CameraX, ML Kit, ONNX Runtime
- Computer Vision: Motion Detection, Pose Detection, MobileSAM
- Video: Recording, Automatic Segment Selection, Precision Trimming

---

<div align="center">
  <strong>TopOut</strong><br />
  등반 기록에 필요한 장면만 더 빠르게.
</div>
