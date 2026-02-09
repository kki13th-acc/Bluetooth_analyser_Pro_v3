# 프로젝트 개요

> **개발 순서: 0단계 - 시작 전 필독**

이 문서는 Bluetooth Analyser Pro V3 프로젝트를 시작하기 전에 전체 구조를 이해하기 위한 개요입니다.

---

## 프로젝트 목표

CFA 포맷의 블루투스 로그를 분석하는 독립 실행형(Standalone) Windows 데스크톱 애플리케이션 개발

---

## 핵심 제약사항

1. **네트워크 격리 환경**: PIP 사용 불가능한 폐쇄망 PC에서 실행
2. **단일 실행파일**: PyInstaller를 통한 .exe 번들링
3. **대용량 로그 처리**: 1GB+ 파일을 효율적으로 처리
4. **직관적인 GUI**: CustomTkinter 기반 모던 UI

---

## 문서 읽기 순서

개발을 시작하기 전에 다음 순서로 문서를 읽어주세요:

### 0단계: 프로젝트 이해
- ✅ `00_PROJECT_OVERVIEW.md` (현재 문서)
- ✅ `../PROJECT_PLAN.md` - 전체 프로젝트 계획

### 1단계: 포맷 이해
- 📄 `01_CFA_FORMAT.md` - CFA 파일 포맷 명세
- 📄 `02_OPCODE_REFERENCE.md` - Bluetooth OPCODE 참조

### 2단계: 설계 이해
- 📄 `03_ARCHITECTURE.md` - 시스템 아키텍처
- 📄 `04_UI_DESIGN.md` - UI 설계

### 3단계: 개발 시작
- 📄 `05_DEVELOPMENT_GUIDE.md` - 개발 가이드

---

## 개발 로드맵 요약

### Phase 1: 코어 엔진 (1-2주)
- CFA 파서
- SQLite 캐싱
- OPCODE 디코더

### Phase 2: GUI 기본 구조 (1주)
- CustomTkinter 메인 윈도우
- 탭 구조
- 파일 오픈 다이얼로그

### Phase 3: 패킷 뷰어 (1-2주)
- Treeview 패킷 리스트
- 상세 정보 패널
- 필터링 기능

### Phase 4: 이슈 검출 (1주)
- 룰 엔진
- 이슈 리스트 UI

### Phase 5: 통합 및 최적화 (1주)
- 전체 시스템 테스트
- 성능 튜닝

### Phase 6: 빌드 및 배포 (3-5일)
- PyInstaller 빌드
- 실행파일 테스트

---

## 주요 기술 스택

| 카테고리 | 기술 | 용도 |
|---------|------|------|
| 언어 | Python 3.9+ | 주 개발 언어 |
| GUI | CustomTkinter | 모던 UI |
| 캐싱 | SQLite3 | 패킷 데이터 캐싱 |
| 배포 | PyInstaller | 단일 실행파일 생성 |

---

## 빠른 시작 가이드

### 1. 저장소 클론
```bash
git clone https://github.com/kki13th-acc/Bluetooth_analyser_Pro_v3.git
cd Bluetooth_analyser_Pro_v3
```

### 2. 가상환경 설정
```bash
python -m venv venv
venv\Scripts\activate  # Windows
```

### 3. 의존성 설치
```bash
pip install -r requirements.txt
```

### 4. 개발 모드 실행
```bash
python src/main.py
```

---

## 주요 디렉토리 구조

```
Bluetooth_analyser_Pro_v3/
├── MD_DOC/             # 📚 프로젝트 문서 (정리됨)
├── src/               # 💻 소스 코드
│   ├── core/         # 핵심 로직
│   ├── analysis/     # 이슈 검출
│   ├── gui/          # GUI 모듈
│   └── utils/        # 유틸리티
├── tests/            # 🧪 테스트
├── assets/           # 🎨 리소스
└── build.spec        # 📦 빌드 설정
```

---

## 다음 단계

1. **`01_CFA_FORMAT.md`** 읽기 - CFA 파일 구조 이해
2. **`05_DEVELOPMENT_GUIDE.md`** 참고 - 개발 환경 설정
3. **Phase 1 시작** - CFA 파서 구현

---

**최종 업데이트**: 2026-02-09
**버전**: V3.0
