# 포트폴리오 웹사이트 — 김민송

PowerPoint(`포트폴리오_김민송.pptx`, 51장)를 웹사이트로 변환한 결과물입니다.

## 바로 보기

`index.html`을 브라우저로 열면 됩니다. 인터넷 연결 없이도 동작합니다.

## 폴더 구성

```
index.html                    사이트 본체 (HTML/CSS/JS 전부 포함)
assets/slides/01.jpg~51.jpg   슬라이드 이미지 (1921×1080)
assets/video/media*.mp4       결과 영상 37개
assets/fonts/                 Pretendard, JetBrains Mono
```

## 사용법

- **스크롤 모드** (기본) — 위에서 아래로 51장을 훑어봅니다
- **발표 모드** — 우측 상단 버튼. 전체화면 한 장씩. `←` `→` 이동, `Esc` 복귀
- **영상 재생** — 슬라이드 위 `▶` 배지를 클릭. 클릭 전에는 다운로드되지 않습니다
- **동시 재생** — 비교 슬라이드(16, 17번 등)는 캡션의 "영상 N개 동시 재생"으로 같은 시점에서 함께 재생됩니다
- **좌측 레일** — 51장 전체 위치 표시. 클릭하면 해당 슬라이드로 이동

## 배포 (GitHub Pages)

```bash
git init && git add . && git commit -m "portfolio site"
git branch -M main
git remote add origin https://github.com/<사용자명>/<레포명>.git
git push -u origin main
```
레포 Settings → Pages → Source를 `main` 브랜치 루트로 지정하면
`https://<사용자명>.github.io/<레포명>/` 에서 열립니다.

## 수정하기

- 슬라이드를 고쳤을 때 → 해당 `assets/slides/NN.jpg`만 교체
- 캡션 문구 → `index.html`에서 `<span class="cap">` 검색
- 상단 소개 문구 → `index.html`의 `<section class="hero">` 부분

## 원본 대비 처리 내역

- 원본 394MB → 90MB (영상을 슬라이드 표시 크기에 맞춰 재인코딩)
- 영상 코덱: H.264 / MP4 (모든 최신 브라우저 지원)
- PowerPoint에서 잘라내기(크롭)된 영상 5개(4, 6, 21번 슬라이드)는 동일한 프레이밍으로 재현
