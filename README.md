# DX11XTK

DirectX 11과 DirectX Tool Kit을 활용한 Windows 그래픽 애플리케이션 프로젝트입니다.

## 요구 사항

- Windows 10 이상
- Visual Studio 2022
- Windows SDK 10.0
- vcpkg (Visual Studio 통합 필요)

## 빌드

1. Visual Studio 2022에서 `DX11XTK.sln` 열기
2. 구성 선택: `Debug|x64` 또는 `Release|x64`
3. 빌드 실행 (Ctrl+Shift+B)

vcpkg 의존성은 빌드 시 자동으로 설치됩니다.

## 프로젝트 구조

| 파일 | 설명 |
|------|------|
| `Main.cpp` | 애플리케이션 진입점, 윈도우 생성 및 메시지 루프 |
| `Game.cpp/h` | 게임 루프, Update/Render 로직 |
| `DeviceResources.cpp/h` | D3D11 디바이스, 스왑체인, 렌더 타겟 관리 |
| `StepTimer.h` | 프레임 타이밍 유틸리티 |
| `pch.h` | 미리 컴파일된 헤더 (DirectXTK 포함) |

## 사용 라이브러리

- **DirectX 11** - 3D 그래픽 API
- **DirectXMath** - SIMD 수학 라이브러리
- **DirectX Tool Kit** - 스프라이트, 모델, 이펙트, 입력 처리 등
- **DirectXTex** - 텍스처 처리 라이브러리

## 참고 자료

- [DirectX Tool Kit Wiki](https://github.com/microsoft/DirectXTK/wiki)
- [DirectXTex Wiki](https://github.com/microsoft/DirectXTex/wiki)
- [DirectX 11 Programming Guide](https://docs.microsoft.com/en-us/windows/win32/direct3d11/atoc-dx-graphics-direct3d-11)

## 라이선스

MIT License
