# IUX Work (iux-app) — 작업 안내서

새로 받아 이어서 고칠 때 먼저 읽는 문서입니다.

## 한 줄 요약
직접 만든 웹서비스·앱을 모아 보여 주는 허브 원페이지. 민왕게임월드(`game` 저장소)의 구조·디자인을 그대로 쓰고 내용만 앱으로 바꿨다.

- 주소: https://app.iux.kr
- 전체 프로젝트 목록: `docs/PROJECTS.md` (모든 저장소·주소·상태를 한곳에 정리)

## 확정된 결정
| 항목 | 결정 |
|---|---|
| 이름 | IUX Work (카테고리 섹션은 없앰) |
| 링크 | GitHub 주소가 아니라 **배포 주소**(iux.kr / vercel.app)로 연결. 주소가 없으면 저장소로 연결 |
| 아이콘 | Lucide |
| 구조 | `index.html` 한 파일, 빌드 없음 |

## 파일
```
index.html     사이트 전체 (APPS 목록 포함)
vercel.json    캐시 헤더
robots.txt, sitemap.xml
docs/PROJECTS.md  전체 프로젝트 목록
```

## 코드 지도 (index.html)
- `var APPS=[...]` — 앱 목록. 항목: `url`(배포 주소), `repo`(저장소), `st`(live·beta·dev), `img`(썸네일, 없으면 `c` 두 색 그라데이션)
- `render`, `item`, `tabs`, `tagsOf` — 목록 그리기 / `recent`, `remember` — 최근 본 앱(localStorage `iux_recent`)
- `hero`, `thumb` — 첫 화면·썸네일 / `spy`, `reveal`, `onScrollFx` — 스크롤 효과
- `<script type="application/ld+json">` — 검색엔진용 앱 목록. APPS를 바꾸면 여기도 맞출 것

## 자주 하는 수정
- **앱 추가:** `APPS`에 한 줄 추가 → JSON-LD 목록과 `sitemap.xml`에도 추가 → `docs/PROJECTS.md`에도 추가

## 브랜치
- `claude/iux-kr-domains`, `claude/add-dalhae-opal` — 내용은 main에 이미 들어간 것으로 보임(정리 시 삭제 가능)

---

## 공통 작업 원칙 (IUX 프로젝트 전체)
- **언어:** 화면 문구·문서·커밋 메시지는 한국어. 쉬운 말, 기술 용어 최소화.
- **퍼블리싱 시안:** 순수 HTML/CSS + 간단한 스크립트만 넣는다. 서버·DB 연동 코드는 개발 단계에서 따로 붙인다.
- **아이콘:** Lucide. 디자인 시스템을 따로 정하지 않았으면 스포티파이 스타일(다크/화이트 + 포인트 컬러)을 기본으로 쓴다.
- **배포:** GitHub `main` → Vercel 자동 배포. 도메인은 가비아 `iux.kr`의 서브도메인(`*.iux.kr` CNAME → Vercel)을 쓴다.
- **DB:** Supabase 무료 플랜은 활성 프로젝트 2개까지라, 새 프로젝트를 만들지 말고 기존 `iux-cloud`(studio) 프로젝트에 테이블을 얹는 것을 먼저 검토한다.
- **비밀값:** 공개 저장소다. 서비스 키·AI 키·비밀번호는 절대 커밋하지 않는다. 키는 Vercel 환경 변수나 Supabase secrets에 둔다. Supabase anon(public) 키만 코드에 넣을 수 있다.
- **확인:** 고친 뒤에는 브라우저 콘솔 오류 0개, 모바일(390px)과 PC 화면을 눈으로 확인하고 나서 완료라고 한다.
- **브랜치:** `main`은 배포 중인 상태. 큰 작업이나 검증 전 작업은 브랜치(`wip/…`, `claude/…`)에 올리고, `main`을 강제 푸시(-f)로 덮어쓰지 않는다.
- **전체 프로젝트 목록:** https://github.com/handgoldking1234/iux-app/blob/main/docs/PROJECTS.md
