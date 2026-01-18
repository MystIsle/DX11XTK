# DX11XTK 프로젝트

## 프로젝트 개요
DirectX 11과 DirectX Tool Kit (DirectXTK)을 사용하는 Windows 데스크톱 게임/그래픽 애플리케이션입니다.

## 기술 스택
- **그래픽 API**: DirectX 11 (d3d11_1, dxgi1_6)
- **수학 라이브러리**: DirectXMath
- **툴킷**: DirectX Tool Kit (DirectXTK)
- **언어 표준**: C++17
- **빌드 시스템**: Visual Studio 2022 (v143 툴셋)
- **패키지 관리**: vcpkg (매니페스트 모드)
- **플랫폼**: Windows 10+ (x64)

## 프로젝트 구조
```
DX11XTK/
├── Main.cpp              # 애플리케이션 진입점 및 윈도우 메시지 처리
├── Game.cpp/h            # 메인 게임 루프 클래스
├── DeviceResources.cpp/h # D3D11 디바이스 및 스왑체인 관리
├── StepTimer.h           # 고정/가변 타임스텝 게임 타이머
├── pch.h/cpp             # 미리 컴파일된 헤더
├── vcpkg.json            # vcpkg 의존성 매니페스트
└── DX11XTK.vcxproj       # Visual Studio 프로젝트 파일
```

## 의존성 (vcpkg)
- `directxmath` - SIMD 수학 라이브러리
- `directxtk` - DirectX Tool Kit (스프라이트, 모델, 이펙트 등)

## 빌드 방법
1. Visual Studio 2022에서 `DX11XTK.sln` 열기
2. vcpkg가 Visual Studio에 통합되어 있어야 함
3. 구성 선택: Debug|x64 또는 Release|x64
4. 빌드 (F7 또는 Ctrl+Shift+B)

## 아키텍처
- **Game 클래스**: `IDeviceNotify` 인터페이스 구현, 게임 루프 및 렌더링 담당
- **DeviceResources**: D3D11 디바이스, 컨텍스트, 스왑체인, 렌더 타겟 관리
- **StepTimer**: Update 호출 타이밍 제어 (고정/가변 타임스텝)

## DirectXTK 기능 (pch.h에 포함됨)
- SpriteBatch/SpriteFont - 2D 스프라이트 및 텍스트 렌더링
- GeometricPrimitive - 기본 3D 도형
- Model - 3D 모델 로딩 및 렌더링
- Effects - 셰이더 이펙트
- Keyboard/Mouse/GamePad - 입력 처리
- CommonStates - 자주 사용하는 렌더 스테이트
- DDSTextureLoader/WICTextureLoader - 텍스처 로딩

## 코딩 컨벤션
- 네임스페이스: `DX` (헬퍼 유틸리티)
- 예외 처리: `DX::ThrowIfFailed()` 사용
- COM 스마트 포인터: `Microsoft::WRL::ComPtr<T>` 사용
- 멤버 변수 접두사: `m_`

## 주의사항
- Windows SDK 10.0 이상 필요
- vcpkg triplet: `x64-windows-static-md` (정적 라이브러리, 동적 CRT)
- DPI 인식: Per-Monitor High DPI Aware
