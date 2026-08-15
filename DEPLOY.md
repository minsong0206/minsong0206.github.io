# GitHub Pages 배포

## 1. 레포 생성
GitHub에서 **New repository** → 이름을 정확히 `minsong0206.github.io` 로 지정 → **Public** 선택
→ README/gitignore/license 체크는 모두 해제 → Create

## 2. 업로드
이 폴더(`portfolio-web`) **안의 내용물**을 레포 루트에 올립니다. 폴더째로 올리면 URL에 경로가 하나 더 붙습니다.

```bash
cd portfolio-web
git init
git add .
git commit -m "portfolio site"
git branch -M main
git remote add origin https://github.com/minsong0206/minsong0206.github.io.git
git push -u origin main
```

용량이 90MB라 push에 몇 분 걸릴 수 있습니다.

## 3. Pages 켜기
레포 **Settings → Pages** →
- Source: **Deploy from a branch**
- Branch: **main** / **/ (root)** → Save

## 4. 접속
1~3분 뒤 https://minsong0206.github.io 에서 열립니다.

---

## 주의사항

- **Git LFS를 쓰지 마세요.** GitHub Pages는 LFS 파일을 서빙하지 않아서 영상이 깨집니다. 일반 파일로 올려야 합니다.
- **무료 플랜은 Public 레포만** Pages를 지원합니다 (Pro 이상은 Private도 가능).
- 사이트 용량 한도는 1GB, 월 트래픽 소프트 한도는 100GB입니다. 현재 90MB라 여유롭습니다.
- 영상 파일을 자주 교체하면 git 히스토리가 계속 커집니다. 교체가 잦아지면 새 레포로 다시 시작하는 편이 낫습니다.

## 프로젝트 페이지로 하고 싶다면

`minsong0206.github.io` 대신 아무 이름(예: `portfolio`)으로 레포를 만들면
`https://minsong0206.github.io/portfolio/` 주소가 됩니다. 나머지 과정은 동일합니다.
