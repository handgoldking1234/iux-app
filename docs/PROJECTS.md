# IUX 전체 프로젝트 목록

저장소를 새로 받아 이어서 작업할 때 보는 지도입니다. 각 저장소의 `CLAUDE.md`(작업 안내서)에 결정사항·코드 지도·수정 방법이 있습니다.
(2026-11-07 기준)

| 서비스 | 저장소 | 주소 | 형태 | 비고 |
|---|---|---|---|---|
| 손금왕 Handgold | [iux-handgold](https://github.com/handgoldking1234/iux-handgold) | handgold.iux.kr | 단일 HTML, AI 없음 | 해석 규칙 `docs/rules.md` |
| IUX Work (앱 허브) | [iux-app](https://github.com/handgoldking1234/iux-app) | app.iux.kr | 단일 HTML | 이 목록이 있는 곳 |
| 민왕게임월드 | [game](https://github.com/handgoldking1234/game) | game.iux.kr | 원페이지 + 게임 HTML, Supabase 통계·대전 | `wip/*` 브랜치 작업 중 |
| IUX.STUDIO / IUX Cloud | [iux-studio](https://github.com/handgoldking1234/iux-studio) | studio.iux.kr | 정적 + Supabase(iux-cloud) | 공용 백엔드. `iux-art-app` 브랜치 미병합 |
| IUX ART | [iux-art](https://github.com/handgoldking1234/iux-art) | art.iux.kr | main 정적 / `nextjs` 브랜치 실서비스 | 작가 사이트 /eunseo /dalhae /opal |
| 웹툰보드 | [iux-webtoon](https://github.com/handgoldking1234/iux-webtoon) | toon.iux.kr | main 단일 HTML / `dev` Next.js | |
| 시놉 | [iux-synop](https://github.com/handgoldking1234/iux-synop) | synop.iux.kr | 단일 HTML | 정본. `synop`은 예전 사본 |
| 교정왕 | [iux-ediking](https://github.com/handgoldking1234/iux-ediking) | ediking.iux.kr | 퍼블리싱 시안 | |
| IUX OCR | [iux-ocr](https://github.com/handgoldking1234/iux-ocr) | ocr.iux.kr | Python 설치형 + 웹 | exe는 Actions가 빌드 |
| ScanQC Web | [iux-qc](https://github.com/handgoldking1234/iux-qc) | qc.iux.kr | 정적 + Supabase | |
| IUX Photo / Illust | [iux-photo](https://github.com/handgoldking1234/iux-photo) | photo.iux.kr | `src/` → 빌드 → 단일 HTML | |
| 하루공부 | [iux-haru](https://github.com/handgoldking1234/iux-haru) | haru.iux.kr | 프로토타입 + Next.js(`web/`) | 문서 `docs/01~09` |
| 우리 가계도 | [iux-son](https://github.com/handgoldking1234/iux-son) | son.iux.kr | 단일 HTML + Supabase | 공개 편집, 검색 차단 |
| AI톡톡 | [iux-aitalk](https://github.com/handgoldking1234/iux-aitalk) | aitalk.iux.kr | 묶음(번들) HTML | 원본 소스 별도 필요 |
| 북이랑 | [bookirang](https://github.com/handgoldking1234/bookirang) | book.iux.kr | 단일 HTML(빌드) + Vercel 함수(Claude) | 초등 영어 북토킹, `booktalk/` 모듈 분리 |
| KoreaTalk | [ktalk](https://github.com/handgoldking1234/ktalk) | ktalk-eta.vercel.app | Flutter + Supabase | Phase 1~12 |
| Seoulmate | [seoulmate](https://github.com/handgoldking1234/seoulmate) | seoulmate.iux.kr | Claude Design 시안 | KoreaTalk 화면 |
| Twinsy | [twinsy](https://github.com/handgoldking1234/twinsy) | iux-twinsy.vercel.app | React(Vite+TS) + Supabase | `DESIGN.md` |
| GlobalTrade | [iux-trade](https://github.com/handgoldking1234/iux-trade) | iux-trade.vercel.app | 퍼블리싱 시안 | |
| IUX ERP | [iux-erp](https://github.com/handgoldking1234/iux-erp) | iux-erp.vercel.app | Claude Design 시안 | |
| 빅트리소프트 리뉴얼 | [bts](https://github.com/handgoldking1234/bts) | — | 퍼블리싱 시안 | studio samples에도 사본 |
| (보관) 시놉 사본 | [synop](https://github.com/handgoldking1234/synop) | — | — | iux-synop과 동일 |
| (보관) 손금왕 옛 이름 | iux-hangold | — | — | iux-handgold로 이전 |

이 표에 없는 오래된 저장소(meta, cloud-AML, MetaMathV3Pub)는 정리 대상에서 뺐습니다.

## 공용 자원
- **도메인:** 가비아 `iux.kr`. 서브도메인은 `*` CNAME → Vercel, 각 Vercel 프로젝트에 `<이름>.iux.kr` 추가
- **Supabase:** `iux-cloud`(studio) 프로젝트를 IUX ART·가계도·게임 대전이 함께 씀 — 스키마를 바꿀 때 다른 서비스 영향 확인
- **메일:** help@ / hello@ (공통), art@ (IUX ART 영업)
