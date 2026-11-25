# 요타사 (YOTASA) 커스터마이즈 기준 문서

이 저장소는 harry0703/MoneyPrinterTurbo의 포크로, 유튜브 채널 **요트쎄오 (@yotasa_ceo, 요트 타는 사람들)** 전용으로 커스터마이즈해 나가는 작업 공간입니다.
코드 수정은 Claude가 GitHub 연결을 통해 담당하고, 대표님은 PC에서 실행과 검수만 합니다.

## 적용된 기본값

| 항목 | 값 | 비고 |
|---|---|---|
| 대본 생성 LLM | Anthropic Claude (`llm_provider = "anthropic"`) | config.example.toml에 반영 완료 (2026-11-26). 첫 실행 시 config.toml에 그대로 복사됨 |
| 소재 소스 | Pexels (`video_source = "pexels"`) | 기본값 유지. 실물 소재는 로컬 파일로 투입 |
| 자막 | Edge (`subtitle_provider = "edge"`) | 기본값 유지 |

## 대표님이 채울 것 (PC 로컬 config.toml에만)

첫 실행하면 config.example.toml이 config.toml로 자동 복사됩니다. config.toml에서 아래 두 가지만 채우면 됩니다.

1. `anthropic_api_key` — https://platform.claude.com/settings/keys 에서 발급
2. `pexels_api_keys` — https://www.pexels.com/api 에서 무료 발급

**주의: API 키가 들어간 config.toml은 절대 GitHub에 올리지 않습니다.** (원본 .gitignore에도 config.toml이 제외돼 있습니다.)

## 운영 원칙

- 소재는 실물 우선: 본인 사진·영상(드라이브 자료)과 중고마켓 서베이 영상을 먼저 쓰고, 스톡은 면허·유지비 같은 일반 정보 콘텐츠에만 보조로 사용
- **매물 소개 영상에 스톡 영상 사용 금지** — 실제 매물과 다른 배가 나오면 허위·과장 문제가 됨
- 대본은 한국 기준으로: 한국 면허 체계, 국내 유지비 감각, 현대요트 기준 정보를 따름 (미국 기준 수치 혼입 주의)
- 발행 전 대표님 검수가 원칙. 자동 발행은 안정화 후 단계적으로 연결
- 채널 포지셔닝: 요트는 관광이 아니라 즐기고 소유하는 문화. 믿을 수 있는 전문가

## 커스터마이즈 로드맵

- [x] Phase 0-1: 포크 생성
- [x] Phase 0-2: LLM 기본값을 Claude로 변경
- [ ] Phase 0-3: PC 설치 후 샘플 숏츠 1개 생성 확인
- [ ] Phase 1: 한국어 음성 기본값, 자막 스타일, 해시태그·제목 프리셋
- [ ] Phase 2: 블로그 시리즈 연동 대본 파이프라인
- [ ] Phase 3: 실물 소재 폴더 규약 정리
- [ ] Phase 4: Shorts·TikTok·릴스 발행 자동화 (검수 후)

## 원본 업데이트 방침

원본 프로젝트가 활발히 개발 중이라, 주기적으로 원본 변경 사항을 확인하고 우리 커스터마이즈와 충돌 없는 범위에서 병합합니다.
