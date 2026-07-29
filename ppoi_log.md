# ppoi 프로젝트 로그 test

> 사업 방향, 개발 완료 현황, 주요 의사결정을 시간 순으로 기록. 매주 또는 주요 변곡점마다 업데이트. Claude와 대화 시작 시 "로그 참조해줘" 한 마디로 컨텍스트 복원 가능.
## 로그
---
추가 수정
### 2026-07-29

- `ppoi_dd_todo_after_yuja.md` 전체 작업 완료
  - Supabase 키(Project URL / anon key / service role key) 수령 완료
  - client / admin `.env.local` 환경변수 교체 완료
  - Vercel 배포 환경 환경변수 등록 완료
  - `RequestBoard.tsx` base URL → `NEXT_PUBLIC_API_URL` 변경 완료
  - 어드민 이중 로그인 제거 완료 (`?admin=true` 로직, ppoi-server 전용 폼/토큰 관리 삭제)
  - 로컬 WiFi 체크리스트에서 ppoi-server 관련 항목 제거 완료
  - ppoi-server repo archive 처리 완료
  - `ppoi_planning.md`, `ppoi_api_list.md`, `ppoi_backend_onboarding.md` 문서 업데이트 완료
  - 최종 검수 완료 (클라이언트 피드/검색/상세, 댓글 시스템, 어드민 단일 로그인, iOS Safari)

### 2026-07-29
- 애널리틱스 작업 완료 (GA4 + Clarity + Mixpanel 3종 통합)
- 모바일 클라이언트(ppoi.kr) QA 완료
- 어드민(admin.ppoi.kr) QA 완료
- 유자 작업 일부 잔여 항목 진행 중

### 2026-07-28

- 유자 Supabase API 작업 완료
- Supabase 마이그레이션(댓글 시스템 포함) 완료
- ppoi-client Vercel 배포 완료 (ppoi.kr)
- ppoi-admin Vercel 배포 완료 (admin.ppoi.kr)
- 아웃핏 자동화 파이프라인 API 작업 진행 중
- 프로젝트 로그 문서(ppoi_log.md) 생성



## 현재 상태 스냅샷
---

업데이트 : 2026-07-29

|영역|상태|
|---|---|
|ppoi-client (ppoi.kr)|✅ Vercel 배포 완료|
|ppoi-admin (admin.ppoi.kr)|✅ Vercel 배포 완료|
|Supabase 백엔드 (outfit/item API)|✅ 유자 작업 완료|
|Supabase 마이그레이션 (댓글 시스템)|✅ 완료|
|**ppoi-server (구 댓글 서버)**|**✅ archive 처리 완료**|
|**클라이언트/어드민 Supabase 연동**|**✅ 완료**|
|아웃핏 자동화 파이프라인 API|⏳ 진행 중|
|SmartStore|⏳ 검증 단계|
|Cafe24 연동|📅 예정|

---
**현재 사업 단계**: 1단계 (아웃핏/아이템 등록 파이프라인 자동화 완성 중)



## 사업 로드맵
---

|단계|내용|상태|
|---|---|---|
|1단계|아웃핏/아이템 등록 파이프라인 자동화|🔄 진행 중|
|2단계|직원 채용1, 자체 쇼핑몰 운영, 비즈모델 표준화|📅 예정|
|3단계|허드슨 영입|📅 예정|
|4단계|여성 버전 확장 + 실제 모델 촬영|📅 예정|
|5단계|브랜드 확장|📅 예정|
|6단계|부산 확장|📅 예정|
|7단계|도쿄/상하이/오사카/베이징 확장|📅 예정|



## 주요 의사결정 로그
---

|날짜|결정 사항|이유|
|---|---|---|
|—|Railway 미사용, Firebase 미사용|Vercel + Supabase로 인프라 통합|
|—|댓글 시스템 자체 구축 (Remark42 대체)|UI 커스터마이징 한계|
|—|댓글 구조: 무제한 중첩 트리 → 선형 체인|UX 단순화|
|—|정렬 탭 "Best" → "랭킹"으로 명칭 변경|—|
|—|랭킹 배지 1~20위 동일 메달 디자인으로 단순화|1~3위 메달/4~20위 숫자 분리에서 변경|
|—|SmartStore 먼저, Cafe24는 조건 충족 후|검증 우선|



## 다음 액션 아이템
---

- [ ] 아웃핏 자동화 파이프라인 API 완성
- [ ] dd 후속 작업 (ppoi_dd_todo_after_yuja.md 체크리스트)
- [x] 랭킹 배지 Figma 디자인 → Claude Code 구현
- [ ] SmartStore 검증 단계 완료 → 상품 등록
- [ ] 블로그 글 작성 (ppoi 왜 만듦, 추구 방향)



## 참고 문서
---

- `ppoi_planning.md` — 서비스 전체 기획
- `ppoi_api_list.md` — API 목록
- `ppoi_dev_history.md` — 개발 상세 히스토리
- `ppoi_dd_todo_after_yuja.md` — 유자 작업 완료 후 dd 할 일
- `ppoi_backend_onboarding.md` — 백엔드 온보딩 가이드
