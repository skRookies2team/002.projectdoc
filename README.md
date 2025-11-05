# 프로젝트 관리 시스템

## 프로젝트 개요
이 프로젝트는 GitHub를 활용한 체계적인 프로젝트 관리 시스템입니다. 회의록, 멘토링 일지, 프로젝트 문서화를 통해 효율적인 협업과 프로젝트 추적을 지원합니다.

## 프로젝트 구조
```
project/
├── README.md                 # 프로젝트 메인 설명서
├── docs/                     # 프로젝트 문서
│   ├── meeting-notes/        # 회의록
│   ├── mentoring-logs/       # 멘토링 일지
│   ├── project-docs/         # 프로젝트 관련 문서
│   └── templates/            # 문서 템플릿
├── src/                      # 소스 코드
├── tests/                    # 테스트 코드
├── .gitignore               # Git 무시 파일
└── LICENSE                  # 라이선스
```

## 주요 기능
- [📝 회의록, CPO, 멘토 미팅 일지 모음집](https://www.notion.so/29dfef49d8d5808bbf8ac9daf51049ac?v=29dfef49d8d58107ab8b000c5ce0b1ba)

- [📚 프로젝트 문서화](https://github.com/skRookies2team/002.projectdoc/tree/main/docs/project-docs)

- [🔄 Git 기반 버전 관리](https://github.com/skRookies2team)

- 📋 이슈 및 작업 추적

- [스크럼일지](https://docs.google.com/spreadsheets/d/1YS4x4WRWZ3d5noXlE6DWmHkJFSJDyHFAtpKdt_6kHb0/edit?pli=1&gid=485940834#gid=485940834)
- [📊 칸반 보드 (JIRA)를 통한 작업 관리](https://pmatal.atlassian.net/jira/software/projects/SCRUM/boards/1?atlOrigin=eyJpIjoiM2ZlZDMxYzI2ZGVmNDk4ODg5ZDJiOTI2NTk1ZDBjNWMiLCJwIjoiaiJ9)


## 시작하기

### 1. 저장소 클론
```bash
git clone [repository-url]
cd project
```

### 2. 문서 작성 가이드
- 회의록: `docs/meeting-notes/` 디렉토리에 작성
- 멘토링 일지: `docs/mentoring-logs/` 디렉토리에 작성
- 프로젝트 문서: `docs/project-docs/` 디렉토리에 작성

### 3. 템플릿 사용
각 문서는 `docs/templates/` 디렉토리의 템플릿을 참고하여 작성하세요.

## GitHub 이슈 관리 (Notion/Jira 대체)

### 칸반 보드 설정
1. **Projects 생성**: GitHub 저장소에서 `Projects` 탭 클릭 → `New project` → `Board` 선택
2. **이슈를 칸반에 추가**: 이슈 생성 후 우측 사이드바의 `Projects`에서 추가
3. **칸반 컬럼 설정**: 기본적으로 `Todo`, `In progress`, `Done` 구조
   - 새로 받은 작업: `Todo`
   - 진행 중: `In progress`
   - 완료: `Done`

**주의**: 이슈를 생성해도 자동으로 칸반 보드가 생성되지 않습니다. GitHub Projects를 별도로 설정해야 합니다.

### 이슈 라벨링
효율적인 관리를 위해 이슈에 라벨을 추가하세요:
- `bug`: 버그 수정
- `feature`: 새로운 기능
- `documentation`: 문서 작업
- `question`: 질문
- `enhancement`: 개선사항

### PR 머지 시 자동 이슈 닫힘
PR 제목이나 본문에 이슈 번호를 포함하면:
- `Fixes #14` 또는 `Closes #14` → PR 머지 시 #14 이슈 자동 종료
- PR 머지 후 해당 이슈는 `Done` 상태로 이동

## 기여하기

### 워크플로우
1. **이슈 생성**: 작업할 내용을 이슈로 생성 (`Issues` → `New issue`)
2. **브랜치 생성**: 이슈 번호를 포함하여 브랜치 생성
   ```bash
   git checkout -b feature/14-user-authentication
   ```
3. **작업 및 커밋**: 이슈 번호를 커밋 메시지에 포함
   ```bash
   git commit -m 'Fix: #14 로그인 기능 수정'
   ```
4. **푸시**: 브랜치를 원격 저장소에 푸시
   ```bash
   git push origin feature/14-user-authentication
   ```
5. **Pull Request 생성**: PR 제목에 이슈 번호 포함 (자동으로 이슈 닫힘)
   - PR 제목: `Fix: #14 로그인 기능 수정` 또는
   - PR 본문에 `Closes #14` 또는 `Fixes #14` 포함

### 이슈 자동 닫힘 키워드
PR 제목 또는 본문에 다음 키워드를 사용하면 PR 머지 시 자동으로 이슈가 닫힙니다:
- `Closes #번호`
- `Fixes #번호`
- `Resolves #번호`
- `해결 #번호`

예시: `Closes #14` → PR 머지 시 #14 이슈 자동 종료

## 라이선스
이 프로젝트는 MIT 라이선스 하에 배포됩니다.

## 연락처
프로젝트 관련 문의사항이 있으시면 이슈를 생성해 주세요.
