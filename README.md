# IUX Work (iux-app)

직접 만든 웹서비스·앱을 모아 둔 원페이지 사이트예요. 민왕게임월드(iuxgame) 구조와 디자인을 그대로 쓰고 내용만 앱으로 바꿨어요.

## 앱 추가·수정
`index.html` 아래쪽 `var APPS=[...]` 에 한 줄 추가하면 돼요.
- `url` 배포 주소 (비어 있으면 '공개 준비 중' 안내)
- `repo` GitHub 저장소 (url이 없으면 저장소로 연결)
- `st` live(바로 쓰기) · beta(베타) · dev(개발 중)
- `img` 썸네일 이미지 경로(선택). 없으면 `c` 두 색 그라데이션 화면이 자동으로 그려져요.

## Vercel 배포
GitHub 저장소 `iux-app`에 올리고 vercel.com → Import → Framework **Other** → Deploy.

## 이어서 작업하기
결정사항·코드 지도·수정 방법은 [CLAUDE.md](CLAUDE.md), 전체 프로젝트 목록은 [IUX 프로젝트 목록](https://github.com/handgoldking1234/iux-app/blob/main/docs/PROJECTS.md)에 있습니다.
