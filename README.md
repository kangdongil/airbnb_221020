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

### 0.4 Django Project 시작하기
- `poetry add django`
- `django-admin startproject config .`

#### 0.4.1 Django Project 구조 살펴보기
- `manage.py`
  - Terminal에서 Django 명령을 실행하게 함
- `db.sqlite3`
  - Development 단계에서 Django가 임시로 사용하는 DB 파일
  - 첫 `runserver` 명령과 함께 자동으로 빈 파일로 생성됨
  - `migration`을 통해 코드에 알맞은 DB 모양이 되도록 동기화함.
- `config/`
  - `config.settings`
    - Django Project 관한 모든 설정이 이뤄지는 파일
  - `config.urls`
    - Django Project의 Url들을 관리하는 파일
    - `include`로 App별 url을 묶어 관리하기 좋다

### 0.4.1 Django Project 설정하기
- `config.settings`
  ```python3
  # To use Server Timezone
  TIME_ZONE = "Asia/Seoul"
  ```
