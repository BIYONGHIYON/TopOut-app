<div align="center">
  <img width="180" height="180" alt="TopOut logo" src="https://github.com/user-attachments/assets/f3f75e67-414c-4a6a-92f2-52b47f9badbd" />

# TopOut

**등반 시작부터 완등 순간까지, 자동으로 찾아주는 클라이밍 촬영 앱**<br>
**From the First Move to the TopOut**

`iOS 출시 완료 · Available on iOS` · `Android 출시 완료 · Available on Android`

<sub>iOS 2.3 build 21 · Android 2.3 versionCode 21</sub>

[App Store](https://apps.apple.com/app/id6790163178) · [Google Play](https://play.google.com/store/apps/details?id=com.topout.cam)

[한국어](#한국어) · [English](#english)
</div>

---

<a id="한국어"></a>

## 한국어

### 소개

**TopOut**은 실내 클라이머를 위한 스마트 등반 영상 녹화 앱입니다.

사용자의 움직임을 기기 안에서 분석해 등반 시작부터 완등 순간까지 필요한 구간을 자동으로 찾아줍니다. 한 번의 영상에 여러 번의 등반이 담겨 있어도 각각의 시도를 구분합니다.

촬영이 끝나면 자동으로 선택된 구간을 확인하고 시작점과 종료점을 세밀하게 조정한 뒤, 원하는 등반 장면만 사진 앱 또는 갤러리에 저장할 수 있습니다. 긴 영상을 다시 돌려보며 장면을 찾고 편집하는 시간을 줄이고 클라이밍에 더 집중해 보세요.

### 주요 기능

- 매트 경계 자동 탐지 및 직접 보정
- 움직임과 자세를 분석해 등반 시작·종료 시점 감지
- 한 번의 촬영에서 여러 등반 시도 자동 구분
- 자동으로 찾은 구간의 시작점·종료점 정밀 조정
- 자동 구간 편집 여백: iOS 앞뒤 3초, Android 시작 전 5초·종료 후 3초 (원본 영상 범위 내)
- 최대 30배 타임라인 확대와 수정 구간 자동 미리보기
- 원하는 등반 장면만 사진 앱 또는 갤러리에 저장
- 저장된 실제 영상을 TopOut 안에서 다시 열어 확인
- iOS 저장본 조회는 최대 20초 안에 확인하고, 확인 실패 시 결과 화면에서 다시 조작 가능
- 녹화 중단과 저장공간 부족 상황에 안전하게 대응
- 장시간 촬영을 위한 실시간 화면 끄기
- 자동 탐지 준비 또는 탑홀드 선택 완료 후 1분간 조작이 없으면 녹화 카운트다운 자동 시작
- 1분 대기 중 기존 선택 안내를 유지하고 자동 시작 직전 5초 동안만 상단 안내 표시

### 9개 언어 지원

TopOut 2.0부터 다음 언어를 지원합니다.

- English
- 한국어
- 日本語
- 简体中文
- 繁體中文
- Français
- Deutsch
- Español
- Português

기본값인 `자동`은 기기의 선호 언어를 따르며, 지원하지 않는 언어에서는 영어를 사용합니다. 설정에서 원하는 언어를 직접 선택할 수도 있습니다.

긴 번역도 버튼 밖으로 나가거나 말줄임표로 숨지 않도록 화면을 조정했습니다. 촬영·선택·결과 안내와 Tip은 화면 너비에 맞춰 한 줄로 표시하면서도, 벽과 매트 사이의 경계와 사용자가 해야 할 조작을 구체적으로 안내합니다.

Android는 버튼 배치를 바꾸지 않고 내부 여백과 아이콘 간격, 자동 축소 범위를 조정해 긴 두 줄 문구도 읽기 좋은 크기로 표시합니다.

### 사용 흐름

```text
촬영 옵션과 구도 설정
→ 매트 경계 자동 탐지 및 직접 보정
→ 직접 녹화 시작 또는 준비 상태 1분 후 자동 시작
→ 기기 내 움직임·자세 분석
→ 여러 등반 구간 자동 제안
→ 시작점·종료점 정밀 조정
→ 원하는 구간만 사진 앱 또는 갤러리에 저장
→ 실제 저장 영상을 TopOut 안에서 확인
```

자동 탐지는 편집을 시작하기 위한 구간을 제안합니다. 감지된 결과는 결과 화면에서 언제든지 직접 확인하고 수정할 수 있으며, 완등이 감지되어도 녹화는 사용자가 종료할 때까지 계속됩니다.

### 기본 촬영 설정

| 항목 | 기본값 |
|---|---|
| 해상도 | FHD |
| 프레임률 | 60fps |
| 화면 비율 | 9:16 |
| 자동 구간 탐지 | ON |
| 탑홀드 마스킹 | OFF |
| 도움말 | ON |
| 녹화 중 실시간 화면 | OFF |

지원 후보는 FHD·4K, 30fps·60fps, 9:16·4:5·3:4·1:1과 세로·가로 촬영입니다. 실제 선택 가능한 조합은 기기의 카메라 성능에 따라 달라질 수 있습니다.

### 플랫폼 및 호환성

#### iOS

- iOS 16.0 이상
- Swift · UIKit · AVFoundation
- Apple Vision · Core ML MobileSAM
- 현재 버전: 2.3 build 21

#### Android

- Android 8.0(API 26) 이상
- Kotlin · Jetpack Compose · CameraX
- MoveNet Thunder · LiteRT · ONNX Runtime MobileSAM
- 현재 버전: 2.3 versionCode 21

기기별 카메라 하드웨어, 지원 포맷, 촬영 환경과 자세 인식 결과에 따라 자동 감지 정확도에는 차이가 있을 수 있습니다.

### 개인정보 및 영상 처리

- 회원가입 없이 사용할 수 있습니다.
- 이름, 이메일 주소, 위치정보를 앱 기능 수행 목적으로 수집하지 않습니다.
- 촬영한 영상과 분석용 이미지 프레임을 TopOut 개발자 서버로 업로드하지 않습니다.
- 움직임 감지, 자세 추정과 매트 경계 탐지는 사용자의 기기 안에서 수행됩니다.
- 사용자가 저장을 선택한 결과 영상만 기기의 사진 앱 또는 갤러리로 내보냅니다.

[TopOut 개인정보 처리방침](https://topoutprivacy.vercel.app/?lang=ko)

### 지원 및 문의

문제 신고나 기능 제안에는 기기 모델, 운영체제 버전, TopOut 버전, 재현 순서와 화면 캡처를 함께 적어 주세요.

- [TopOut 고객지원](https://biyonghiyon.github.io/TopOut-app/?lang=ko)
- [GitHub Issues](https://github.com/BIYONGHIYON/TopOut-app/issues)
- 이메일: [byeonghyeon383@gmail.com](mailto:byeonghyeon383@gmail.com)

### TopOut 2.3

- 앱이 촬영 중 강제 종료되며 남긴 임시 영상을 다음 실행 때 자동으로 정리해 저장공간 확보
- iOS: 촬영 시작·녹화 종료·결과 재생 전환 때 오디오 설정으로 화면이 잠시 멈출 수 있던 문제 개선
- iOS: 통화 등으로 마이크나 소리를 쓸 수 없을 때도 영상 촬영과 결과 재생은 계속 진행
- Android: 시작 화면을 고정 시간 없이 카메라가 준비되는 즉시 닫아 앱 진입을 iOS와 같은 흐름으로 정리

### TopOut 2.2

- 자동 탐지 준비 또는 탑홀드 선택 완료 후 1분 동안 녹화 시작을 누르지 않으면 자동으로 카운트다운 시작
- 조각난 매트 영역도 같은 상단 직선으로 이어지면 함께 분석하고 위·아래로 튀는 부분을 제외해 경계 탐지 안정성 개선
- 카메라·분석·녹화·저장·리뷰의 취소와 리소스 정리 경로 개선
- Android 자동 감지 구간의 편집 여백을 시작 전 5초·종료 후 3초로 조정
- iOS·Android 선택 구간 타임라인의 확대 상한을 30배로 확장

### TopOut 2.1

- 벽과 매트 사이 경계, 파란 점 조작, 시작~완등 구간 안내를 9개 언어에서 더 구체적으로 개선
- 작은 화면에서도 촬영·선택·결과 안내와 Tip이 한 줄로 보이도록 자동 축소 유지

### TopOut 2.0

- 앱 UI를 9개 언어로 제공하고 자동·수동 언어 선택 지원
- 매트 분석이 5초 안에 끝나지 않으면 기본 경계와 직접 보정 화면으로 복구
- 여러 등반 시도 자동 구분과 결과 구간 편집 흐름 개선
- 시작점 수정 후 해당 위치부터, 종료점 수정 후 3초 전부터 자동 미리보기
- 선택 구간 확대 슬라이더의 전체 트랙 터치와 즉시 드래그 지원
- 실제 Photos·MediaStore 저장 항목을 다시 열어 저장 결과 확인
- 저사양 기기의 앱 시작, 메모리와 장시간 녹화 안정성 개선
- 화면 가장자리의 잘린 자세를 새 등반으로 잘못 인식하는 경우 완화
- Android 멀티 렌즈 줌과 다양한 카메라 구성 대응 강화
- iOS·Android의 긴 다국어 문구와 가로·세로 UI 대응 보강
- 벽·매트 경계 보정과 결과 구간 안내를 9개 언어에서 더 구체적으로 개선

### 저장소 안내

이 저장소는 TopOut의 공개 소개, 고객지원, 개인정보 처리방침과 업데이트 안내를 위한 저장소입니다. App Store 및 Google Play 배포용 앱 소스와 내부 탐지 파라미터는 별도의 비공개 저장소에서 관리합니다.

[맨 위로](#topout)

---

<a id="english"></a>

## English

### About TopOut

**TopOut** is a smart climbing video recorder built for indoor climbers.

It analyzes movement on your device and automatically finds the useful part of each attempt—from the start of your climb to the send. If one recording contains multiple attempts, TopOut separates them into individual clips.

After recording, review the suggested clips, fine-tune their start and end points, and save only the moments you want to Photos or your gallery. Spend less time searching through long videos and more time climbing.

### Key Features

- Automatic mat boundary detection with manual correction
- On-device movement and pose analysis for climb start and end detection
- Automatic separation of multiple attempts in one recording
- Precise start and end point adjustment
- Automatic clip padding: 3 seconds on each side on iOS; 5 seconds before and 3 seconds after on Android, within the source video bounds
- On iOS, saved-video lookup is limited to 20 seconds; review controls recover if verification fails
- Up to 30× timeline zoom and automatic preview after trim changes
- Save only selected climbing clips to Photos or your gallery
- Open the actual saved video again inside TopOut
- Safe recording finalization during interruptions or low-storage conditions
- Optional live-preview shutdown for long recording sessions
- Automatic recording countdown when Start Recording is not tapped for one minute after detection setup is ready

### Available in 9 Languages

Starting with TopOut 2.0, the app supports:

- English
- 한국어
- 日本語
- 简体中文
- 繁體中文
- Français
- Deutsch
- Español
- Português

The default `Automatic` option follows your device’s preferred language and falls back to English when the language is not supported. You can also choose a language manually in Settings.

Layouts keep longer translations visible instead of overflowing or being replaced with ellipses. Camera, selection, review, and Tip guidance stays on one line while clearly identifying the wall–mat boundary and the action the user should take.

### How It Works

```text
Choose recording options and frame your wall
→ Detect or manually correct the mat boundary
→ Start recording manually, or automatically after one ready minute
→ Analyze movement and pose on the device
→ Suggest clips for multiple climbing attempts
→ Fine-tune each start and end point
→ Save only the clips you want to Photos or your gallery
→ Open the actual saved video again in TopOut
```

Automatic detection provides a starting point for editing. You can always review and adjust the suggested clips. Recording continues after a send is detected and stops only when you choose to finish.

### Default Recording Settings

| Setting | Default |
|---|---|
| Resolution | FHD |
| Frame rate | 60fps |
| Aspect ratio | 9:16 |
| Automatic clip detection | ON |
| Top-hold masking | OFF |
| Help | ON |
| Live preview while recording | OFF |

Potential options include FHD or 4K, 30fps or 60fps, 9:16·4:5·3:4·1:1, and portrait or landscape recording. Available combinations depend on the device’s rear-camera capabilities.

### Platforms and Compatibility

#### iOS

- iOS 16.0 or later
- Swift · UIKit · AVFoundation
- Apple Vision · Core ML MobileSAM
- Current version: 2.3 build 21

#### Android

- Android 8.0(API 26) or later
- Kotlin · Jetpack Compose · CameraX
- MoveNet Thunder · LiteRT · ONNX Runtime MobileSAM
- Current version: 2.3 versionCode 21

Detection accuracy may vary with camera hardware, supported formats, filming conditions, and pose-estimation results.

### Privacy and Video Processing

- No account or sign-up is required.
- TopOut does not collect your name, email address, or location to provide app features.
- Recorded videos and analysis frames are not uploaded to a TopOut developer server.
- Movement detection, pose estimation, and mat boundary detection run on your device.
- Only the clips you choose to save are exported to Photos or your gallery.

[TopOut Privacy Policy](https://topoutprivacy.vercel.app/?lang=en)

### Support and Contact

When reporting a problem, please include your device model, operating-system version, TopOut version, reproduction steps, and a screenshot when possible.

- [TopOut Support](https://biyonghiyon.github.io/TopOut-app/?lang=en)
- [GitHub Issues](https://github.com/BIYONGHIYON/TopOut-app/issues)
- Email: [byeonghyeon383@gmail.com](mailto:byeonghyeon383@gmail.com)

### TopOut 2.3

- Automatically removes temporary videos left by a forced quit during recording on the next launch to free storage
- iOS: Prevents brief UI freezes caused by audio setup when the camera starts, recording ends, or review playback begins
- iOS: Keeps recording video and playing review clips when the microphone or audio output is in use by a call
- Android: Closes the launch screen as soon as the camera is ready instead of after a fixed delay, matching the iOS startup flow

### TopOut 2.2

- Starts the recording countdown automatically when Start Recording is not tapped for one minute after setup is ready
- Keeps the normal selection guidance during the wait and shows an automatic-start notice only for the final five seconds
- Improved mat-boundary stability by combining disconnected regions that support the same upper line while excluding vertical outliers
- Improved cancellation and resource cleanup across camera, analysis, recording, saving, and review flows
- Changed Android automatic clip padding to five seconds before and three seconds after each detected attempt
- Increased selected-range timeline zoom to a maximum of 30× on iOS and Android

### TopOut 2.1

- Clarified wall–mat boundary, blue-point adjustment, and start-to-finish review guidance in all nine languages
- Kept camera, selection, review, and Tip guidance on one line with automatic text scaling on small screens

### TopOut 2.0

- Added a 9-language interface with automatic and manual language selection
- Added a five-second mat-analysis fallback with immediate manual correction
- Improved multi-attempt detection and review editing
- Added automatic preview from the new start point or three seconds before the new end point
- Enabled full-track touch and immediate dragging on the timeline zoom slider
- Reopens the actual Photos or MediaStore item to verify saved videos
- Improved startup, memory use, and long-recording stability on constrained devices
- Reduced false climb starts caused by partial poses near screen edges
- Improved Android multi-lens zoom and support for varied camera configurations
- Improved long translated labels and portrait·landscape layouts on both platforms
- Clarified wall–mat boundary correction and review guidance in all nine languages

### Repository

This repository contains TopOut’s public product introduction, support information, privacy policy, and release updates. The App Store and Google Play application source and internal detection parameters are maintained in a separate private repository.

[Back to top](#topout)

---

<div align="center">
  <strong>TopOut</strong><br />
  등반 시작부터 완등 순간까지, 자동으로 찾아주는 클라이밍 촬영 앱<br />
  From the First Move to the TopOut
</div>
