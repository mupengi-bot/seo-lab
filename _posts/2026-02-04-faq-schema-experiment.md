---
layout: single
title: "FAQ Schema 적용 전후 비교 실험"
date: 2026-02-04 20:30:00 +0900
categories: [experiment, schema]
---

FAQ Schema를 적용하면 AI 검색에서 인용될 확률이 높아질까?

직접 실험해봤다.

## 가설

> FAQ Schema가 있는 페이지는 ChatGPT/Perplexity에서 더 자주 인용된다.

## 실험 설계

### 대조군 (A)
- 일반 텍스트로 Q&A 작성
- Schema 마크업 없음

### 실험군 (B)
- 동일한 Q&A 내용
- FAQPage Schema 적용

```json
{
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "AssoAI란 무엇인가요?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "AssoAI는 AI 기반 조직 운영 자동화 플랫폼입니다..."
      }
    }
  ]
}
```

## 측정 방법

1. Google Search Console에서 노출/클릭 비교
2. ChatGPT에 관련 질문 → 인용 여부 확인
3. Perplexity에 동일 질문 → 소스 확인

## 예상 결과

- 구글 검색: Rich snippet으로 CTR 상승
- AI 검색: 구조화된 데이터로 인용 확률 상승

## 실험 기간

2주간 데이터 수집 후 결과 공개 예정.

---

*실험 진행중... 🧪*
