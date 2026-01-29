# 📂 ResourceHub (리소스 허브)

**Sogarian Projects**를 위한 공용 정적 자원(이미지, 미디어) 호스팅 리포지토리입니다.

## 🌟 개요
이 저장소는 여러 프로젝트에서 공통으로 사용하는 이미지나 미디어 파일을 저장하고, **jsDelivr CDN**을 통해 전 세계에 빠르게 배포하기 위해 존재합니다.

*   **Public Access**: 이 저장소는 공개(Public)되어 있으며, 업로드된 파일은 누구나 접근 가능합니다.
*   **CDN Driven**: 직접 GitHub Raw 링크를 사용하는 대신, `cdn.jsdelivr.net`을 통해 트래픽을 분산하고 속도를 최적화합니다.

## 🚀 사용 방법

### 1. 이미지 저장 규칙
*   **경로:** `data/images/hosted/YYYY/MM/DD/`
*   **파일명:** 중복 방지를 위해 원본 파일의 Hash(MD5) 값을 주로 사용합니다.

### 2. CDN 링크 구조
GitHub에 파일을 업로드하면 즉시 아래 주소로 접근할 수 있습니다.

```
https://cdn.jsdelivr.net/gh/sogarian/ResourceHub@main/data/images/hosted/2026/01/29/example.jpg
```

*   `@main`: 브랜치명 (필요시 특정 태그나 버전을 지정 가능)

## 🤖 자동화 (AssetOps)
이 저장소는 주로 AI Agent의 **`GitHubAssetManager`** 모듈에 의해 자동으로 관리됩니다.
1.  Agent가 외부 이미지를 수집
2.  이 저장소로 자동 Commit & Push
3.  서비스에는 CDN 링크로 반환

---
⚠️ **주의:** 민감한 개인정보나 보안 키 파일은 절대 이 저장소에 업로드하지 마십시오.
