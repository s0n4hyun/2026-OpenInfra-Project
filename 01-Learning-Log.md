# 01. Git/GitHub 및 Sphinx·tox 학습 기록

## 1. Git/GitHub

Git은 코드의 변경 내역을 관리하는 도구이고, GitHub는 코드를 온라인에 저장하고 다른 사람과 공유하는 서비스이다.

- **Fork** : 다른 사람의 GitHub 저장소를 내 계정으로 복사
- **Clone** : GitHub 저장소를 내 컴퓨터로 가져오기
- **Branch** : 기존 코드를 유지하면서 별도로 작업할 수 있는 공간
- **Commit** : 수정한 내용을 하나의 기록으로 저장
- **Push** : 내 컴퓨터에서 작업한 내용을 GitHub에 업로드
- **Pull Request(PR)** : 수정한 내용을 원본 저장소에 반영해 달라고 요청
- **Merge** : 서로 다른 브랜치의 변경 내용을 합치기

### 직접 실습한 내용

Sphinx 문서 구조를 구성하고 tox를 이용한 HTML 문서 빌드에 성공했다. Git Branch를 생성해 작업한 내용을 Commit, Push함.

## 2. Sphinx와 tox

- **reStructuredText(rST)** : 기술 문서를 작성할 때 사용하는 문서 형식
- **Sphinx** : `.rst` 문서를 HTML 웹페이지로 변환하는 도구
- **tox** : 필요한 실행 환경을 준비하고 정해진 명령어를 자동으로 실행하는 도구

### 주요 파일

| 파일 | 역할 |
|---|---|
| `conf.py` | Sphinx의 기본 설정 |
| `index.rst` | 웹페이지의 첫 화면 |
| `requirements.txt` | 필요한 Python 패키지 목록 |
| `tox.ini` | 자동 빌드 명령어 설정 |
| `.gitignore` | Git에 올리지 않을 파일 지정 |

### 주요 명령어

```bash
git branch
git switch docs-setup
git add .
git commit -m "Add basic Sphinx documentation setup"
git push -u origin docs-setup
```

```bash
python -m tox -e docs
```

마지막 명령어는 tox를 이용해 Sphinx HTML 문서를 빌드할 때 사용한다.

## 3. 오류를 통해 배운 점

- **경로 오류** : 터미널의 현재 위치에 따라 파일을 찾는 경로가 달라진다.
- **파일 중복 오류** : Clone하려는 폴더가 이미 존재하면 다른 이름을 지정해야 한다.
- **인코딩 오류** : 파일의 문자 인코딩이 다르면 한글을 읽는 과정에서 오류가 발생할 수 있다.
- **가상환경 오류** : Python 패키지는 현재 사용하는 실행 환경에 설치되어 있어야 한다.

처음에는 GitHub의 Fork, Clone, Branch가 각각 어떤 역할을 하는지 헷갈지만 직접 저장소를 복사하고 브랜치를 만들어 작업하면서 차이를 이해할 수 있었다.

또한 Sphinx와 tox를 이용해 문서 빌드 환경을 구성하고, GitHub에 코드를 업로드하는 과정을 경험했다. 특히 여러 오류를 해결하면서 터미널의 현재 경로와 파일 구조를 정확하게 확인하는 것이 중요하다는 것을 알게 되었다.
