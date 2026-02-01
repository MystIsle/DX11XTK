# DX11XTK - Sprites and Textures

DirectX 11과 DirectX Tool Kit을 활용한 스프라이트 및 텍스처 렌더링 예제입니다.

## 브랜치 정보

**현재 브랜치**: `feature/Sprites-and-textures`

이 브랜치에서는 SpriteBatch를 사용한 2D 스프라이트 렌더링과 텍스처 로딩을 구현합니다.

## 구현 기능

- **SpriteBatch**: 2D 스프라이트 일괄 렌더링
- **텍스처 로딩**: DDS, WIC(PNG, JPG) 포맷 지원
- **배경 이미지**: WICTextureLoader로 JPG 배경 로딩
- **스프라이트 이미지**: DDSTextureLoader로 DDS 텍스처 로딩

## 리소스 파일

| 파일 | 설명 |
|------|------|
| `Resources/cat.dds` | 고양이 스프라이트 (DDS 포맷) |
| `Resources/cat.png` | 고양이 원본 이미지 |
| `Resources/sunset.jpg` | 배경 이미지 |
| `Resources/texconv.exe` | DirectXTex 텍스처 변환 도구 |

## 요구 사항

- Windows 10 이상
- Visual Studio 2022
- Windows SDK 10.0
- vcpkg (Visual Studio 통합 필요)

## 빌드

1. Visual Studio 2022에서 `DX11XTK.sln` 열기
2. 구성 선택: `Debug|x64` 또는 `Release|x64`
3. 빌드 실행 (Ctrl+Shift+B)

## 사용 라이브러리

- **DirectX 11** - 3D 그래픽 API
- **DirectXMath** - SIMD 수학 라이브러리
- **DirectX Tool Kit** - SpriteBatch, 텍스처 로더 등
- **DirectXTex** - 텍스처 처리 및 변환

## 참고 자료

- [DirectXTK Wiki - SpriteBatch](https://github.com/microsoft/DirectXTK/wiki/SpriteBatch)
- [DirectXTK Wiki - DDSTextureLoader](https://github.com/microsoft/DirectXTK/wiki/DDSTextureLoader)
- [DirectXTK Wiki - WICTextureLoader](https://github.com/microsoft/DirectXTK/wiki/WICTextureLoader)

## 라이선스

MIT License
