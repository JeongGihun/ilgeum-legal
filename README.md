# legal_site — 읽음 약관·개인정보 정적 페이지

Play Console / OAuth 동의화면에 등록할 **개인정보처리방침·이용약관·회원탈퇴 안내** 정적 HTML.

- `index.html` — 3종 링크 허브
- `terms.html` — 이용약관
- `privacy.html` — 개인정보처리방침 (수집항목·권한·보관/삭제·유출통지)
- `withdrawal.html` — 회원탈퇴 안내

빈칸 채움: 시행일 `2026-07-18` · 운영자 `정기훈` · 문의 `solux3501@gmail.com` · 마이크 미사용 · HTTPS(TLS) 반영.
외부 의존 없음(인라인 CSS) — 어디에 올려도 그대로 뜬다.

## GitHub Pages로 무료 호스팅 (도메인 불필요)

> ⚠️ `project_book` 레포가 **private면 Pages 무료가 안 된다**(GitHub Pro 필요). 그래서 **전용 public 레포**를 새로 판다.

```bash
# 1) GitHub에서 public 레포 생성: 예) ilgeum-legal
# 2) 이 폴더 내용만 그 레포에 올린다
cd legal_site
git init
git add .
git commit -m "읽음 약관·개인정보 정적 페이지"
git branch -M main
git remote add origin https://github.com/<사용자>/ilgeum-legal.git
git push -u origin main
```

3. 레포 **Settings → Pages → Source: `Deploy from a branch` → Branch: `main` / `/ (root)`** 저장.
4. 1~2분 뒤 공개 URL:
   - 개인정보처리방침: `https://<사용자>.github.io/ilgeum-legal/privacy.html`
   - 이용약관: `https://<사용자>.github.io/ilgeum-legal/terms.html`
   - 회원탈퇴: `https://<사용자>.github.io/ilgeum-legal/withdrawal.html`

## 등록처

- **Play Console**: 앱 콘텐츠 → 개인정보처리방침 URL = 위 `privacy.html` 주소
- **Data safety form**: 수집 항목(이메일 식별자·독서기록·업로드 이미지), 카메라 권한, 제3자 미제공, 전송 암호화(HTTPS) 기준으로 작성
- **OAuth 동의화면(Google)**: 개인정보처리방침 URL·이용약관 URL 각각 등록

## 갱신

문안 원본은 앱 내 `mobile/src/app/legal.tsx`와 동일 계열. 문구를 고치면 이 HTML도 같이 갱신하고 재푸시한다. 정식 출시 전 전문가(노무사/변호사) 검토 권장.
