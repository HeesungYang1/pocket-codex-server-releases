# Pocket Codex Server — Android 배포

이 저장소는 Pocket Codex Server의 Android ARM64 설치 파일만 공개 배포합니다. 애플리케이션 소스 코드는 이 저장소에 포함하지 않습니다. APK에는 앱 실행에 필요한 코드와 Android용 런타임이 포함됩니다.

## 파일

각 공개 GitHub Release에는 아래 두 파일만 게시합니다.

- `pocket-codex-server-vX.Y.Z-arm64.apk` — Android ARM64용 설치 APK
- `pocket-codex-server-vX.Y.Z-arm64.apk.sha256` — APK의 SHA-256 체크섬

릴리스는 사전 릴리스로 표시될 수 있습니다. 버전과 테스트 범위는 각 릴리스 설명을 확인하세요.

## 설치와 업데이트

Android ARM64 기기에서 릴리스 APK를 내려받아 설치하세요. 파일 관리자나 브라우저에서 설치가 차단되면 Android 설정에서 해당 앱의 **알 수 없는 앱 설치 허용**을 켜야 할 수 있습니다. 기존 앱을 업데이트할 때는 서명 키를 유지한 APK를 사용하세요. Android 시스템 설치 화면에서 설치를 마지막으로 확인해야 합니다.

v0.5.0의 비공개 업데이터는 이 공개 저장소를 찾지 못하므로 v0.6.0으로 처음 전환할 때는 공개 릴리스에서 APK를 직접 내려받아 기존 앱 위에 설치하세요. v0.6.0 이후 지원 버전은 토큰 없이 공개 릴리스를 확인합니다. 업데이트 확인에 인터넷 연결이 필요하며, 다운로드와 설치는 사용자가 선택합니다.

## Android 호환성과 앱 데이터

Pocket Codex는 Termux 기반 런타임을 앱에 포함하며 Android 패키지 이름은 com.termux입니다. 공식 Termux도 같은 패키지 이름을 사용하므로 두 앱을 함께 설치할 수 없습니다. 기존 공식 Termux가 설치되어 있다면 설치를 취소하고 기존 앱이나 데이터를 삭제하지 마세요. 서명 키가 달라 기존 공식 앱 위에 이 APK를 설치할 수 없을 수 있습니다. 이 릴리스는 Android ARM64 (rm64-v8a) 기기용입니다.

## SHA-256 확인

릴리스의 `.sha256` 파일에 적힌 체크섬과 APK 파일의 체크섬이 같은지 확인하세요. Windows PowerShell에서는 다음을 실행할 수 있습니다.

```powershell
Get-FileHash .\pocket-codex-server-vX.Y.Z-arm64.apk -Algorithm SHA256
```

Linux, macOS 또는 Termux에서는 다음을 사용할 수 있습니다.

```sh
sha256sum pocket-codex-server-vX.Y.Z-arm64.apk
```

## 지원 범위

이 배포 채널은 Android ARM64 설치 파일용이며 Google Play 배포가 아닙니다. 실제 기기 호환성, 검증 범위와 알려진 제한은 각 릴리스 노트에서 확인하세요.