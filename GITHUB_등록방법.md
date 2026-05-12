# 🚀 GitHub 등록 가이드

이 폴더(`github-repo`)의 파일을 GitHub에 등록하는 방법 두 가지를 안내합니다.

---

## ✅ 방법 1: GitHub 웹 (가장 쉬움, 추천)

GitHub 명령어를 사용하지 않고 웹 브라우저에서만 등록하는 방법입니다.

### 1단계: GitHub 저장소(Repository) 생성

1. https://github.com 로그인
2. 우측 상단 `+` → **New repository** 클릭
3. 다음과 같이 입력:
   - **Repository name** : `hwaseong-contract-manual` (또는 원하는 이름)
   - **Description** : `화성시 사업담당자 계약업무 매뉴얼 (인터랙티브)`
   - **Public** 또는 **Private** 선택 (Public 권장 — 공공기관 자료)
   - ✅ **Add a README file** 체크 해제 (이미 있음)
   - **Add .gitignore** : None
   - **License** : None
4. **Create repository** 클릭

### 2단계: 파일 업로드

1. 생성된 저장소 페이지에서 **"uploading an existing file"** 링크 클릭
   (또는 `Add file` → `Upload files`)
2. 다음 3개 파일을 드래그&드롭:
   - `index.html`
   - `README.md`
   - `.gitignore`
3. 페이지 하단에 커밋 메시지 입력:
   ```
   Initial commit: 화성시 사업담당자 계약업무 매뉴얼 v1.0
   ```
4. **Commit changes** 클릭

### 3단계: GitHub Pages 활성화 (선택, 권장)

웹에서 바로 매뉴얼을 사용할 수 있도록 무료 호스팅을 활성화합니다.

1. 저장소 페이지 상단 **Settings** 클릭
2. 좌측 메뉴 **Pages** 클릭
3. **Source** 설정:
   - Branch: `main` 선택
   - Folder: `/ (root)` 선택
4. **Save** 클릭
5. 1~2분 후 https://[사용자명].github.io/hwaseong-contract-manual/ 에서 접속 가능

---

## ✅ 방법 2: Git 명령어 (개발자용)

로컬 PC에 `github-repo` 폴더를 다운로드받은 후 터미널에서 진행:

```bash
# 폴더로 이동
cd github-repo

# git 초기화
git init
git branch -M main

# 파일 추가
git add .
git commit -m "Initial commit: 화성시 사업담당자 계약업무 매뉴얼 v1.0"

# 원격 저장소 연결 (GitHub에서 만든 저장소 URL로 교체)
git remote add origin https://github.com/[사용자명]/hwaseong-contract-manual.git

# 푸시
git push -u origin main
```

### 인증 방법
- **HTTPS 방식** : GitHub Personal Access Token 사용
  - https://github.com/settings/tokens 에서 토큰 발급
  - `repo` 권한 체크 후 발급된 토큰을 비밀번호 대신 입력
- **SSH 방식** : `~/.ssh/id_rsa.pub` 등록 (https://github.com/settings/keys)

---

## 📦 포함된 파일

| 파일 | 설명 |
|---|---|
| `index.html` | 메인 매뉴얼 (124KB, 단일 HTML 파일) |
| `README.md` | GitHub에 표시될 프로젝트 설명 |
| `.gitignore` | Git 무시 파일 목록 |
| `GITHUB_등록방법.md` | 이 가이드 |

---

## ⚠️ 주의사항

### Public 저장소로 공개할 경우
- 매뉴얼 내부에 **실제 담당자 이름·연락처는 포함되지 않습니다** (모두 placeholder)
- localStorage에 저장되는 담당자 정보는 **사용자 개인 브라우저에만 저장**되므로 GitHub에 업로드되지 않습니다
- 안심하고 공개 가능합니다

### 저장소 이름 추천
- `hwaseong-contract-manual` (영문, 권장)
- `hwaseong-contract-form` (서식 강조)
- `hwaseong-bigdata-tools` (팀 도구 모음)

### 향후 업데이트
파일을 수정한 뒤 다시 업로드하면 자동으로 GitHub Pages에 반영됩니다 (1~2분 소요).

---

## 🆘 문제 해결

### "이미 같은 이름의 저장소가 있습니다"
- 다른 이름으로 만들거나 기존 저장소 삭제 후 재시도

### "GitHub Pages에 접속이 안 됩니다"
- Settings → Pages에서 활성화 확인
- 5분 정도 기다린 후 재시도
- 브라우저 캐시 삭제

### "파일이 너무 큽니다"
- index.html은 124KB로 GitHub 제한(100MB) 내 안전

---

**개발** : 화성시 빅데이터팀 (신환철 · 전명구 · 이동재 · 김지현 · 지우근 · 이주희)
