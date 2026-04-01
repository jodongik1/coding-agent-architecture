# Oh My Cap (omc) 🧢

**엔터프라이즈 폐쇄망 전용 Agentic AI 코딩 어시스턴트 플러그인 프로젝트 (Architecture & Docs)**

이 저장소는 공공/금융 등 완벽한 보안망(폐쇄망) 환경을 유지하면서도 능동적인 유지보수를 지원하는 **'Oh My Cap (omc)' IDE 통합형 에이전틱 AI 코딩 플러그인**의 설계도, 아키텍처 다이어그램 및 기획(요구사항) 문서를 관리하는 깃허브입니다.

## 📖 주요 목표 (Core Objectives)
1. **망분리(Air-gapped) 환경 특화:** 외부 인터넷 연결 없이 오직 내부망 사내 LLM 서버와 연동 (데이터 유출, 텔레메트리 원천 차단).
2. **에이전틱 자율성 (Plan/Act 모드):** 채팅봇 수준을 넘어 AI가 스스로 이슈를 분석하고 다중 소스코드를 자율적으로 수정/테스트.
3. **개발자 통제(Persona) 강화:** 역할별 맞춤 페르소나와 사용자 지정(우클릭) 프롬프트 매크로 등을 통해 완전한 사용자 시스템 제어권 보장.
4. **레거시 코드 매니지먼트:** 다중 파일 연계(Impact) 분석, 정적/보안 취약점 스캔, SQL 정합성 검사 등 실무 E2E 환경 조준.

## 📂 저장소 문서 구조도 (Directory Structure)
- **`0.0.intro.md`**: 전반적인 개발 프로세스 단계(SDLC)와 각 마일스톤 소개 요약본
- **`1.1.prd.md`** : 상세 제품 요구사항 정의서 (*저장소 커밋 현황에 따라 파일명 변경 가능성 있음*)
- **`1.2.wireframe.md`** : IntelliJ 기준의 시각화 기획 (메인 채팅 패널, 동적 설정 5탭, 컨텍스트 메뉴 매크로 뷰)
- **`assets/`** : 사용자 스토리 기반의 목업 이미지 모음

## ⚙️ 타겟 시스템 워크플로우 (Target Tech Stack)
- **Client (플러그인 프론트):** IntelliJ IDEA Ultimate / Community (v2021.2 이상)
- **Backend (에이전트 제어 프록시):** LangGraph 기반 State Machine 모델링 (Python)
- **LLM/통신 Server:** NVIDIA DGX 로컬 서버(Port 11434 기준) / REST API Streaming (OpenAI API Spec 완벽 호환)

## 🚀 향후 마일스톤 (Roadmap)
- [x] Phase 1. 제품 요구사항(PRD) 및 UI 와이어프레임 설계 확정
- [ ] Phase 2. 시스템 아키텍처 및 OpenAPI 규격 정의 (Tool Calling, PSI Parser 통신 명세)
- [ ] Phase 3. 랭그래프(LangGraph) 기반 핵심 에이전트 라우팅 / 상태 머신 서버 로직 코딩
- [ ] Phase 4. IntelliJ 플러그인 프론트 UI 개발 및 JIRA 등 사내 이슈 트래커 결합
- [ ] Phase 5. QA (망분리 통신 검사 및 OOM 스트레스 테스트) 후 Zip 배포

---
**Oh My Cap(omc)**은 단순한 RAG 봇이나 코드 자동완성 툴(Copilot)을 넘어, "시니어 자바 개발자"를 가상 팀원으로 영입하여 레거시 유지보수의 전 주기를 함께 해결하는 엔터프라이즈 AI 코어 파트너입니다.
