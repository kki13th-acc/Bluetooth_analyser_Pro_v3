# Bluetooth Analyser Pro V3 - 문서

> **Bluetooth Core Specification 6.2 지원**
> 
> 이 프로젝트는 CFA 포맷의 Bluetooth 로그를 분석하는 독립 실행형 Windows 애플리케이션입니다.

---

## 📚 문서 읽기 순서

### 신규 개발자
1. **00_PROJECT_OVERVIEW.md** - 프로젝트 전체 개요 (필독)
2. **01_CFA_FORMAT.md** - CFA 파일 포맷 명세
3. **02_OPCODE_REFERENCE.md** - Bluetooth OPCODE 참조
4. **03_ARCHITECTURE.md** - 시스템 아키텍처
5. **04_UI_DESIGN.md** - UI 설계 가이드
6. **05_DEVELOPMENT_GUIDE.md** - 개발 가이드

---

## 📖 문서 목록

### 핵심 문서
| 문서 | 설명 | 읽기 시간 |
|------|------|----------|
| 00_PROJECT_OVERVIEW.md | 프로젝트 개요 및 목표 | 10분 |
| 01_CFA_FORMAT.md | CFA 파일 포맷 완전 명세 | 20분 |
| 02_OPCODE_REFERENCE.md | Bluetooth OPCODE 테이블 | 15분 |
| 02_OPCODE_PARAMETERS.md | OPCODE 파라미터 상세 | 30분 |
| 03_ARCHITECTURE.md | 시스템 아키텍처 설계 | 15분 |
| 04_UI_DESIGN.md | GUI 설계 및 구현 가이드 | 20분 |
| 05_DEVELOPMENT_GUIDE.md | 개발 환경 및 구현 가이드 | 15분 |

---

## 🎯 프로젝트 핵심 목표

### 성능
- ✅ 1GB 파일을 **2초 이내** 오픈
- ✅ 100만 패킷도 **60 FPS** 부드러운 스크롤
- ✅ 메모리 사용량 **500MB 이하**

### 기능
- ✅ Bluetooth Core 6.2 **완전 지원**
- ✅ HCI Commands/Events **완벽 디코딩**
- ✅ LE Audio (CIS/BIS) 분석
- ✅ **TOP 14 이슈 시나리오** 자동 검출

### 사용성
- ✅ 직관적인 CustomTkinter UI
- ✅ 네트워크 격리 환경 지원 (독립 실행 파일)
- ✅ 프로그레스 바로 로딩 단계 실시간 표시

---

## 🏗️ 기술 스택

| 카테고리 | 기술 | 버전 | 용도 |
|---------|------|------|------|
| 언어 | Python | 3.9+ | 주 개발 언어 |
| Spec | Bluetooth Core | 6.2 | 프로토콜 명세 |
| GUI | CustomTkinter | Latest | 모던 UI |
| DB | SQLite3 | Built-in | 패킷 캐싱 |
| Build | PyInstaller | Latest | 단일 실행파일 |

---

## 📈 개발 로드맵

### Phase 1: 코어 엔진 (2주)
- CFA Parser
- Lazy Loading
- SQLite Cache
- Progress Reporting

### Phase 2: Bluetooth 디코딩 (2주)
- OPCODE Registry
- HCI Commands (150+)
- HCI Events (60+)
- LE Audio Support

### Phase 3: GUI 기반 (2주)
- Main Window
- Virtual Scrolling
- Threading Model

### Phase 4: 패킷 뷰어 (2주)
- Packet List
- Detail Panel
- Filter Engine

### Phase 5: 이슈 검출 (2주)
- Rule Engine
- Suspect Issue Tab
- JSON Config Loader
- 14개 이슈 룰 구현

---

## 🔗 참조

- [Bluetooth Core Spec 6.2](https://www.bluetooth.com/specifications/specs/core-specification-6-2/)
- [GitHub Repository](https://github.com/kki13th-acc/Bluetooth_analyser_Pro_v3)

---

**최종 업데이트**: 2026-02-09
**버전**: V3.0
