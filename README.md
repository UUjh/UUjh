# 안녕하세요 :wave:
### 유저에게 좋은 기억을 남기고 싶은 Unity 개발자입니다 :whale:

:ocean: 긍정적이고 끈기 있는 자세로 문제를 끝까지 해결합니다.<br/>
:ocean: 기능 구현을 넘어 안정적인 상태 흐름과 사용자 경험을 고민합니다.<br/>
:ocean: 함께하는 팀이 믿고 맡길 수 있는 든든한 개발자가 되고 싶습니다.<br/>

<div align="center">
<br/>
<h2>About Me :runner:</h2>

[![Notion](https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=Notion&logoColor=white)](https://app.notion.com/p/maintaining/JiHyun-Yoo-41644e42e5864cc198cada6b21961cf4)
[![Tistory](https://img.shields.io/badge/Tistory-000000?style=for-the-badge&logo=Tistory&logoColor=white)](https://maintaining.tistory.com/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=GitHub&logoColor=white)](https://github.com/UUjh)

<br/>
<h2>Tech Stack</h2>

#### Main

![Unity](https://img.shields.io/badge/Unity-000000?style=for-the-badge&logo=unity&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-DD2C00?style=for-the-badge&logo=firebase&logoColor=white)
![Photon](https://img.shields.io/badge/Photon-004480?style=for-the-badge&logo=photon&logoColor=white)
![Steamworks](https://img.shields.io/badge/Steamworks-000000?style=for-the-badge&logo=steam&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

`UniTask` · `R3` · `MessagePipe` · `Addressables` · `Input System` · `Localization` · `Spine` · `DOTween`

#### Additional Experience

![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Android Studio](https://img.shields.io/badge/Android%20Studio-3DDC84?style=for-the-badge&logo=android-studio&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)

</div>

<br/>

## Experience at a Glance

- Steam 출시 프로젝트 3종 개발. 이 중 2종은 기획부터 출시까지 단독 개발
- Firebase REST 기반 모바일 아웃게임 클라이언트 개발. 서버 권위 경제, `requestId` 멱등 재시도, 세션 격리
- Photon PUN2 / Fusion, Steamworks, STOVE, Addressables, Spine 연동
- 출시 이후 사용자 환경에서 발생한 문제 대응과 업데이트 경험
- 자동 테스트가 없던 프로젝트에 EditMode 테스트를 도입하고 AI 리뷰의 검증 게이트로 운용
- `CLAUDE.md` / `AGENTS.md`, 리뷰 에이전트, 훅, UnityMCP로 AI 보조 개발 환경 구성

---

## Selected Projects

<div align="center">

| 프로젝트 | 플랫폼 | 역할 | 상태 |
|:---:|:---:|:---:|:---:|
| 🐧 Project T | Android / iOS | 클라이언트 담당 | 개발 중 |
| 🐱 Meow's Meow | Windows | 기획 · 단독 개발 | 2025.09 Steam 출시 |
| 👻 WHO'S WHO 2.0 | Windows | 메인 개발자 | 2025.03 Steam 출시 |
| 🏕️ Cozy Night | Windows | 단독 개발 | 2024.11 Steam 출시 |

</div>

### 🐧 Project T

> 모바일 파티 퀴즈 게임<br/>
> 팀 프로젝트 · 클라이언트 담당 · Spread It · 2026.04 ~ 개발 중

[![Sample Code](https://img.shields.io/badge/Sample_Code-181717?style=for-the-badge&logo=GitHub&logoColor=white)](https://github.com/UUjh/SampleCode4)

캐릭터 커스터마이징과 실시간 트리비아 퀴즈를 결합한 모바일 게임입니다.
아웃게임은 Firebase Cloud Functions REST, 게임 방은 Photon Fusion이 담당합니다.

#### 주요 기여

- Firebase Cloud Functions REST API 기반 클라이언트 개발
- 재화 · 아이템 · 점수 · 랭킹의 최종값을 서버 응답으로만 확정하는 서버 권위 구조. 보상 처리 순서를 `캐시 반영 → 영수증 저장 → 연출`로 고정
- `requestId` 멱등 재시도로 구매 · 가챠 중복 결제 방지. 인증 오류 복구와 분리하고 실패 시 재화 재동기화
- 세션 세대 검증과 요청 소유자 각인으로 계정 간 데이터 혼입 차단
- Bootstrap과 Catalog 분리. 카탈로그 SHA-256 검증 · 로컬 캐시 · 버전 불일치 복구
- 서버 확정 보상만 연출하고 미수령 보상을 복구하는 흐름 구성
- 전체 장비 슬롯 스냅샷 기반 장착 상태 동기화
- Scene · Prefab 창을 한 경로로 여는 타입 기반 UI Window 생명주기. route stack 뒤로가기와 동시 작업 직렬화, 예외 시 정리 흐름
- Addressables Sprite 참조 횟수 관리와 안전한 해제 처리
- 다양한 모바일 해상도에 대응하는 UI와 Spine 캐릭터 표시
- EditMode 테스트 도입. 약 25,000줄 아웃게임을 `차단 관계 → 중복 증식 차단 → 재작업 최소화` 순으로 점진 리팩터링

#### AI 활용

- Dryforge를 사용한 AI 하네스 엔지니어링
- 프로젝트 루트와 모듈 디렉터리에 계층형 `AGENTS.md` 구성. 모듈별 불변 조건 기록
- 아키텍처 · 도메인 규칙 · 보안 · 운영 문서와 ADR 유지, 코드베이스 위키 컴파일
- UnityMCP를 Unity Editor에 연결하여 상태 확인과 작업에 활용
- Unity CLI를 이용한 EditMode 테스트 실행과 결과 검증
- Claude와 Codex 교차 검토로 서버 계약과 코드 대조. AI 제안은 코드 변경점, 테스트, 로그를 기준으로 최종 검증

#### Tech

`Unity 6` `C#` `Firebase` `Photon Fusion`
`UniTask` `R3` `MessagePipe` `Addressables` `Spine` `Unity Test Framework`

---

### 🐱 Meow's Meow

> 데스크톱 펫 게임<br/>
> 기획 및 단독 개발 · Night Vendors Studio · 2025.06 ~ 2026.04 · 2025.09 Steam 출시 · 리뷰 22개 긍정 100%

[![Steam](https://img.shields.io/badge/Steam-000000?style=for-the-badge&logo=steam&logoColor=white)](https://store.steampowered.com/app/3953340/Meows_Meow/)
[![Sample Code](https://img.shields.io/badge/Sample_Code-181717?style=for-the-badge&logo=GitHub&logoColor=white)](https://github.com/UUjh/SampleCode2)

#### 주요 기여

- 투명 창 · 다중 모니터 전환 · 항상 위 설정을 처리하는 Windows 데스크톱 오버레이 구현
- Move / Climb / Decision 상태 기반 고양이 행동 FSM 개발. 클릭 보상 · 캐릭터 드래그 · 먹이 주기 · 장난감 및 가구 상호작용과 액세서리 꾸미기 구현
- ScriptableObject 기반 캐릭터 · 오브젝트 데이터. 유저 · 설정 · 배치 · 구매 · 투두를 단일 저장 계층에서 관리
- 할 일, 알람, 스티커 메모 및 작업 시간 관리 기능 구현
- 라디오, 로컬 음악 재생 및 미니 플레이어 구성
- 파일 드래그 앤 드롭, 휴지통, Windows 프로그램 · 폴더 실행 등 데스크톱 연동
- Steam / STOVE / None을 빌드 시 선택하는 빌드 프로세서와 배치 빌드 인자, 테스트 빌드용 세이브 경로 분리
- Steam 도전 과제, 클라우드 저장 및 다국어 기능 연동. 출시 후 스킨 · 음악 · 라디오 콘텐츠 추가

#### Tech

`Unity 6` `C#` `Spine` `Win32 API` `NAudio`
`DOTween` `Steamworks.NET` `STOVE` `Input System` `Localization`

---

### 👻 WHO'S WHO 2.0

> 온라인 멀티플레이 파티 게임<br/>
> 팀 프로젝트 · 메인 개발자 · Night Vendors Studio · 2024.05 ~ 2025.06 · 2025.03 Steam 출시 · 리뷰 214개 긍정 83%

[![Steam](https://img.shields.io/badge/Steam-000000?style=for-the-badge&logo=steam&logoColor=white)](https://store.steampowered.com/app/3391260/WHOS_WHO_20/)
[![Sample Code](https://img.shields.io/badge/Sample_Code-181717?style=for-the-badge&logo=GitHub&logoColor=white)](https://github.com/UUjh/SampleCode1)

NPC 사이에 숨은 진짜 플레이어를 찾아내 탈락시키는 3D 캐주얼 액션 PVP. 11개 모드, 6개 언어, F2P.
출시 후 신규 캐릭터 · DLC 추가까지 진행한 뒤 유지보수를 후임에게 인계했습니다.

#### 주요 기여

- Bomb, Gift, 무궁화꽃이 피었습니다 등 게임 모드를 룰 단위로 분리해 개발
- 로비, 게임 룸, 결과 화면, 연결 해제 및 Master Client 변경 흐름 구현
- RPC 기반 멀티플레이 게임 상태와 UI 동기화. 충돌 기반 전투 판정과 모드 · 팀 규칙 반영
- 캐릭터 스킬, 애니메이션, 이펙트, 사운드 및 스킨 시스템 개발. NPC 스폰과 룸 초기화
- 키보드 · 컨트롤러 입력 통합, 리바인딩, 진동 및 디바이스별 UI 대응
- Steam 도전 과제, DLC 및 언어 설정 연동
- 출시 이후 버그 수정과 플레이 안정화, 신규 콘텐츠 추가 후 인계

#### Tech

`Unity 2022 LTS` `C#` `Photon PUN2` `Steamworks.NET`
`Input System` `Localization` `NavMesh` `URP`

---

### 🏕️ Cozy Night

> 계절과 사운드를 감상하는 인터랙티브 힐링 콘텐츠<br/>
> 이전 회사에서 개발이 중단된 프로젝트를 개인 프로젝트로 이어서 완성<br/>
> 단독 개발 · 2024.04 ~ 2025.07 · 2024.11 Steam 출시 · 리뷰 17개 긍정 100%

[![Steam](https://img.shields.io/badge/Steam-000000?style=for-the-badge&logo=steam&logoColor=white)](https://store.steampowered.com/app/3159090/Cozy_Night/)

#### 주요 기여

- 개발 중단 이후 남은 기능 구현과 Steam 출시 준비를 직접 진행
- 클릭 · 정기 · 체류 이벤트 베이스를 상속하는 환경 이벤트 시스템. 시간에 따른 이벤트와 여름 · 겨울 전환
- 북극곰과 범고래의 등장 연출 및 클릭 상호작용 개발
- 배경음, 환경음과 라디오 콘텐츠 구성. MP3, WAV, OGG 파일을 불러오는 사용자 BGM 기능
- JSON 직렬화 게임 데이터 저장 · 초기화 및 Steam 도전 과제 연동
- 출시 후 Unity 2022.3에서 Unity 6로 이전, 사용자 피드백을 반영한 기능 추가와 업데이트

#### Tech

`Unity 6` `C#` `Steamworks.NET`
`DOTween` `Cinemachine` `UnityWebRequest` `URP`

---

<h2 align="center"> 🤖 AI-Assisted Development 🤖 </h2>

:robot: AI 활용 능력은 질문을 많이 하는 것보다 AI가 프로젝트의 문맥, 권한, 검증 절차를 따르도록 구성하는 능력이라고 생각합니다.<br/>
:robot: Claude와 Codex를 코드 작성자가 아니라 리뷰어로 두고, 검증 게이트를 통과한 변경만 받아들입니다.

#### 🛡️ Guardrails
- 리뷰어 역할, 승인 없는 수정 금지, push · merge · reset 금지를 전역 규칙으로 명시
- 지적은 위치 · 근거 · 영향 · 재현 조건 · 확신도를 갖춰야 확정. 근거가 약하면 '확인 필요'로 낮춤
- P0~P3 우선순위 기준. 크래시 · 데이터 손상 · 보안 문제만 P0
- 비밀 정보와 내부 서버 주소는 AI 문맥과 공개 문서에서 제외

#### 🧭 Context Engineering
- 저장소 루트 `CLAUDE.md` / `AGENTS.md`에 문서 지도와 철칙, 모듈별 `AGENTS.md`에 불변 조건 기록
- 아키텍처 · 도메인 규칙 · 보안 · 강제 규칙 · 함정 모음 · 운영 · 외부 계약 문서와 ADR 유지
- 코드베이스 위키를 도구로 컴파일하고 커버리지 태그로 원본 확인 필요 여부 표시
- 재지적 금지 항목과 서버 계약을 에이전트 메모리로 관리해 같은 리뷰가 반복되지 않게 함

#### 🧰 Tooling
직접 만들거나 구성해서 실제로 쓰는 도구들입니다.

| 도구 | 용도 |
|---|---|
| UnityMCP · Unity CLI | Claude · Codex에서 에디터 상태와 오브젝트 구성, 현재 프로젝트 상황을 직접 확인. EditMode 테스트를 실행하고 결과로 AI 리뷰를 검증 |
| 커스텀 리뷰 에이전트 4종 | 구조 · 성능 · 안정성/보안 · 정리 관점의 독립 리뷰. Claude용 `.md`와 Codex용 `.toml`을 같은 내용으로 구성 |
| `object-design` 커스텀 스킬 | 객체 설계 학습노트를 스킬로 정리해 책임 배분 · 과설계 판정 기준으로 사용. Codex에도 이식 |
| 컨텍스트 감시 훅 | 컨텍스트 30% 경고 · 40% 강한 경고 후 5%p마다 재경고, 자동 compact 창 설정. Claude는 PostToolUse · Stop, Codex는 UserPromptSubmit에 등록 |
| 상태줄 스크립트 | 모델 · 컨텍스트 사용률 · 5시간 / 주간 한도 리셋 시각 표시 |
| llm-wiki-compiler | 코드베이스 위키 컴파일과 증분 갱신. 커버리지 태그로 원본 확인 필요 여부 표시 |
| dryforge | 리팩터링 마이그레이션 계획과 ready 리뷰, HTML 감사 리포트 |
| diagram-design | UML · 구조 다이어그램을 HTML로 만들어 책임 분리 검토와 세미나 자료에 사용 |
| 병렬 서브에이전트 | 챕터별 문서 분석, 역할별(시니어 개발자 · 인사 · PM) 교차 검토, 모듈별 코드 감사 |
| Unity 공식 스킬 · find-skills | Unity 공식 스킬을 설치하고 작업에 맞는 스킬을 탐색해 조합할 수 있는 환경 구성 |
| 설정 이식 저장소 | claude-config · codex-portable로 규칙 · 에이전트 · 스킬 · 훅 · 메모리를 Mac ↔ Windows에 동일하게 설치 |

- 작업 성격에 따라 모델과 추론 강도를 바꿔 씁니다. 분석 · 감사는 높은 추론 강도, 단순 편집은 낮은 강도
- 리뷰 리포트 · 다이어그램 · 학습노트는 단독 HTML로 산출해 브라우저와 폰에서 그대로 열람

#### 🔁 Cross-Model Review
- Claude와 Codex에 같은 규칙을 주고, 구조 · 성능 · 안정성/보안 · 정리 4개 관점의 리뷰 에이전트로 독립 검토
- 읽기 전용 리뷰 하네스 구성. 두 모델의 리뷰를 세 번째 프롬프트가 비교해 최종 우선순위 정리

#### ✅ Verification
- AI 감사 결과는 EditMode 테스트 통과 여부로 검증. 테스트가 없던 프로젝트에 테스트부터 도입
- UnityMCP로 에디터 상태를 확인하고 Unity CLI로 테스트 실행
- PR 본문은 설계 질문 7개에 답하는 형식. 보호할 불변식, 정보를 가진 객체, 추상화가 제거하는 복잡성, 없어도 되는가, 유지할 행위, 검증 테스트, 제외할 정리

```text
요구사항 · 제약 정의 → 프로젝트 문맥 로드 → Claude · Codex 분석 및 교차 리뷰
→ 개발자 구현 → EditMode 테스트 · 에디터 검증 → 개발자 최종 판단 → 문서화
```
