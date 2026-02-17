<p align="center">
  <img src="https://raw.githubusercontent.com/HWP2RAG/.github/main/Logo.png" alt="HWPtoRAG" width="120" />
</p>

<h1 align="center">HWPtoRAG</h1>

<p align="center">
  <b>HWP 문서를 AI/RAG에 최적화된 형태로 변환합니다</b><br/>
  Native Parsing & Agentic Reconstruction
</p>

<p align="center">
  <a href="https://hwptorag.com">Website</a> ·
  <a href="https://hwptorag.com/docs/getting-started">Docs</a> ·
  <a href="https://hwptorag.com/pricing">Pricing</a>
</p>

---

## 왜 HWPtoRAG인가?

한국에서 생산되는 공공 · 법률 · 학술 문서의 상당수는 HWP(한글) 포맷입니다.
그러나 LlamaParse, Unstructured.io, Azure Document Intelligence 등 주요 AI 문서 처리 도구는 **HWP를 지원하지 않습니다.**

HWPtoRAG는 이 문제를 해결합니다.

- **Rust 기반 네이티브 파싱** — HWP 바이너리를 직접 파싱하여 PDF 변환 없이 원본 구조를 보존합니다
- **AI/RAG 최적화 출력** — Markdown, JSON, RAG-JSON 등 LLM이 바로 사용할 수 있는 포맷으로 변환합니다
- **표 · 이미지 · 메타데이터 인식** — 복잡한 한글 문서의 표, 이미지, 스타일 정보를 정확하게 추출합니다

## 제품

### Web Converter

iLovePDF 스타일의 웹 변환기. 파일을 드래그앤드롭하면 Markdown/JSON으로 변환됩니다.

- 비로그인으로 바로 사용 (하루 5회 무료)
- 최대 100MB 파일 지원
- 4가지 출력 포맷: Markdown · JSON · Plain Text · RAG-JSON

### Python SDK

개발자를 위한 프로그래매틱 API.

```python
from hwptorag import HWPConverter

converter = HWPConverter(api_key="...")
result = converter.convert("document.hwp", format="markdown")
print(result.content)
```

## 기술 아키텍처

| 계층 | 기술 |
|------|------|
| Frontend | Next.js · React · shadcn/ui |
| Backend API | FastAPI · Python |
| Parsing Engine | hwp-rs (Rust) · WASM |
| Storage | Cloudflare R2 / AWS S3 |
| SDK | Python (PyPI) |

## 요금제

| Plan | 가격 | 대상 |
|------|------|------|
| **Community** | 무료 | 개인 사용자 (5회/일) |
| **Pro** | $14.99/월 | 대학원생 · 연구자 |
| **Developer** | $29/월 | API 연동 개발자 |
| **Business** | $199/월 | 팀 · 기업 |
| **Enterprise** | 문의 | 온프레미스 · 대규모 |

## Repositories

| Repo | 설명 |
|------|------|
| [frontend](https://github.com/HWP2RAG/frontend) | 웹 프론트엔드 (Next.js) |
| [BM](https://github.com/HWP2RAG/BM) | 기획서 및 비즈니스 문서 |

## 타겟 사용자

- **대학원생 · 연구자** — 학위 논문, 학술 자료 HWP → Markdown 변환
- **리걸테크** — 법률 문서, 판례 분석을 위한 구조화
- **AI 스타트업** — RAG 파이프라인에 HWP 문서 통합
- **공공기관** — 행정 문서 디지털 전환

---

<p align="center">
  <sub>Made with Rust & AI in Korea</sub>
</p>
