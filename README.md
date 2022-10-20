## 0.0 개발환경 구축하기
### 0.1 Git 설정하기
- `git init`
- `touch .gitignore`
  - [Python_GitIgnore](https://raw.githubusercontent.com/github/gitignore/main/Python.gitignore)
- `git remote add origin [REPOSITORY_URL}`

### 0.2 Python 3.8^ 설치하기

### 0.3 Python VENV: Poetry 설치하기
- `curl -sSL https://install.python-poetry.org | python3 -`
- `poetry init`
- `poetry shell`
- `poetry add --dev black`

#### 0.3.1 Poetry 살펴보기
- `poetry init`: 프로젝트를 poetry가 관리하게 하기
- `poetry add [PACKAGE]`: poetry로 package 설치하기
- `poetry shell`: shell 진입하기
- `exit`: shell 나가기
- `pyproject.toml`: 프로젝트의 명세와 의존성 관리하는 파일