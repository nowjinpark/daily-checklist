## Language

- [English](./README.md)
- [한국어](./README.ko.md)

# Daily Checklist

이 프로젝트는 제가 처음으로 vibe coding 방식으로 만든 단일 파일 데일리 체크리스트 앱입니다. 백엔드나 계정 없이 브라우저에서 바로 날짜별 할 일을 관리할 수 있도록 만들었습니다.

## 프로젝트 소개

처음에는 개인적인 생산성 도구로 시작했지만, 점점 날짜 기반 뷰, 여러 종류의 태스크 동작, 로컬 백업 기능까지 포함한 더 풍부한 체크리스트 앱으로 발전했습니다. 포트폴리오 공개용 버전에서는 개인 백업 파일과 로컬 전용 데이터가 저장소에 포함되지 않도록 정리했습니다.

추천 GitHub 저장소 설명 문구:

> Single-file vibe-coded daily checklist app with date-based planning, recurring duration tasks, local backup, and browser-only storage.

## 주요 기능

- 날짜별로 분리된 체크리스트와 카테고리 관리
- 항상 존재하는 기본 `Daily` 카테고리
- 여러 종류의 태스크 지원
- `Regular`: 선택한 날짜에만 보이는 일반 태스크
- `Daily (Independent)`: 매일 보이지만 완료 여부는 날짜별로 따로 관리
- `Daily (Shared)`: 매일 보이며 어느 날이든 완료하면 전체에서 제거
- `Duration`: 기간을 설정해 여러 날짜에 표시되고, 주간/월간/연간 반복 가능
- 드래그 앤 드롭으로 태스크 순서 변경 및 카테고리 간 이동
- 태스크 제목과 설명을 수정할 수 있는 상세 모달
- 색상과 투명도 조절로 시각적 구분 가능
- 완료된 `Daily (Shared)` 태스크를 위한 휴지통 흐름
- 브라우저에서 JSON 백업 내보내기

## 기술 스택

- HTML
- CSS
- Vanilla JavaScript
- 브라우저 `localStorage` 기반 클라이언트 저장

## 호환성

- Windows와 macOS에서 모두 사용할 수 있습니다
- Chrome, Safari, Arc 같은 최신 브라우저에서 실행됩니다
- 별도 설치 없이 브라우저에서 정적 앱을 열어 바로 사용할 수 있습니다

## 개인정보 및 데이터 처리

- 앱 데이터는 브라우저의 `localStorage`에 저장됩니다.
- 백엔드, 데이터베이스, 외부 API를 사용하지 않습니다.
- 개인 백업 JSON, 스크린샷, 복구/디버그용 파일은 이 저장소에 포함되지 않습니다.

## 실행 방법

정적 앱이라서 아래 두 방법 중 하나로 실행할 수 있습니다.

1. 브라우저에서 `index.html`을 직접 엽니다.
2. 또는 아무 정적 서버로 이 폴더를 서빙합니다.

Python 예시:

```bash
python -m http.server 8000
```

그다음 `http://localhost:8000` 을 열면 됩니다.

## 프로젝트 구조

```text
.
|-- index.html
|-- README.md
|-- README.ko.md
`-- .gitignore
```

## 중점적으로 만든 부분

- 실제 일상 계획 방식에 맞는 태스크 동작 설계
- 프레임워크 없이 클라이언트 상태를 직접 관리하는 구조
- 드래그 앤 드롭과 모달 기반의 인터랙션 구현
- 개인 데이터를 공개 저장소에서 제외한 포트폴리오 정리

## 앞으로 개선하고 싶은 점

- 단일 HTML 파일을 HTML, CSS, JavaScript 파일로 분리
- 공개 버전에 더 정돈된 import/restore 흐름 추가
- 접근성과 모바일 사용성 개선
- 태스크 생성 및 반복 로직에 대한 가벼운 테스트 추가
