# 세특 주제 선정 및 예상 보고서 작성 도우미

숭신고등학교 진로진학상담부 김강석 선생님이 제작한 세특 도우미를 Vercel에 배포하는 프로젝트입니다.

---

## 배포 방법 (Vercel + GitHub)

### 1단계 — GitHub에 올리기

1. [github.com](https://github.com) 에 로그인
2. 우측 상단 **+** → **New repository** 클릭
3. 이름 입력 (예: `seteuk-helper`) → **Create repository**
4. 이 폴더 전체를 업로드 (또는 git push)

### 2단계 — Vercel에 배포하기

1. [vercel.com](https://vercel.com) 에 접속 → GitHub 계정으로 로그인
2. **Add New Project** → 방금 만든 GitHub 저장소 선택
3. **Deploy** 클릭 (설정 변경 없이 그대로)
4. 배포 완료! 자동으로 URL이 생성됩니다 (예: `https://seteuk-helper.vercel.app`)

### 3단계 — API 키 설정하기 (가장 중요!)

1. Vercel 대시보드 → 프로젝트 선택
2. **Settings** 탭 → **Environment Variables**
3. 아래 값 추가:
   - **Name**: `ANTHROPIC_API_KEY`
   - **Value**: `sk-ant-api03-...` (본인의 API 키)
4. **Save** 클릭
5. **Deployments** 탭 → 최신 배포 우측 **...** → **Redeploy**

### API 키 발급

[console.anthropic.com](https://console.anthropic.com) 에서 가입 후 발급 가능합니다.
처음 가입 시 무료 크레딧이 제공됩니다.

---

## 파일 구조

```
seteuk-vercel/
├── api/
│   └── claude.js       ← Claude API 프록시 (API 키는 여기서 사용)
├── public/
│   └── index.html      ← 앱 화면
├── vercel.json         ← Vercel 설정
└── README.md
```

---

## 주의사항

- API 키는 절대 `index.html`이나 코드에 직접 넣지 마세요.
- Vercel 환경변수로만 관리하면 안전합니다.
- API 사용량에 따라 요금이 발생할 수 있습니다.
-
