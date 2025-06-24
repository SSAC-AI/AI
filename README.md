# 📘 AI 학습 정리
## 1. About GitHub, Markdown, Colab
- [GitHub 사용법](#github-사용법)
- [Markdown 문법](#markdown-문법)  
- [Colab 기초](#colab-기초)

## GitHub 사용법

### ✅ GitHub 계정 만드는 순서 (2025년 기준)

1. **웹 브라우저 열기**
   크롬(Chrome), 엣지(Edge), 사파리(Safari) 중 편한 걸 사용하세요.

2. **GitHub 웹사이트 접속**
   주소창에 아래 주소를 입력하고 Enter 누르세요: https://github.com

3. **회원가입 시작하기**
   화면 오른쪽 위 또는 중간에 있는 Sign up 버튼 클릭

4. **이메일 주소 입력**
   평소 자주 사용하는 이메일을 입력

5. **비밀번호 만들기**
   영어 대문자, 소문자, 숫자, 특수문자를 섞어 안전하게!
   예시: Git1234!hub

6. **사용자 이름(Username) 정하기**
   나만의 고유한 이름을 지어요 (다른 사람이 쓰고 있으면 불가)
   - 예시: jetsunmom, sungsookjang66 등
   - 영어, 숫자, 하이픈(-) 가능 (띄어쓰기 ❌)

### ✅ Repository 만들기 순서

1. **GitHub에 로그인 후 New Repository 클릭**
2. ![new](https://github.com/user-attachments/assets/3481a680-f677-403b-be8c-1fe59d5aa7cb)
3. **Repository 이름 입력**
4. **Public/Private 선택**
5. **README.md 파일 생성 체크**
6. **Create repository 버튼 클릭**
   
![create_repository](https://github.com/user-attachments/assets/8c2eb16b-8dfc-465a-88cd-d35770d12df0)

## Markdown 문법
---
### 🔰 1. 마크다운(Markdown)이란?

Markdown은 글을 **쉽게 꾸미기 위한 문법**이에요. HTML보다 간단하게 **제목, 목록, 굵은 글씨, 링크, 코드블록** 등을 작성할 수 있어요.
GitHub에서는 `README.md` 파일을 통해 마크다운을 많이 사용합니다.

---

### 🛠️ 2. GitHub에서 마크다운 사용하려면?

1. **GitHub 계정**을 만들고
2. 새 **Repository**를 만든 뒤
3. `README.md` 파일을 추가해서
4. 마크다운 문법을 사용하여 내용을 입력하면 됩니다.

---

### ✍️ 3. 기본 마크다운 문법 정리

| 기능        | 문법               | 예시                         | 결과                       |
| --------- | ---------------- | -------------------------- | ------------------------ |
| 제목(Title) | `#`, `##`, `###` | `## 내 프로젝트`                | 내 프로젝트                   |
| 굵게        | `**굵게**`         | `**중요**`                   | **중요**                   |
| 기울임       | `*기울임*`          | `*강조*`                     | *강조*                     |
| 목록        | `-`, `*`         | `- 사과` <br> `- 배`          | ● 사과 <br> ● 배            |
| 숫자 목록     | `1.`, `2.`       | `1. 첫째` <br> `2. 둘째`       | 1. 첫째 <br> 2. 둘째         |
| 링크        | `[이름](주소)`       | `[구글](https://google.com)` | [구글](https://google.com) |
| 이미지       | `![이름](이미지주소)`   | `![고양이](cat.jpg)`          | ![고양이](cat.jpg)          |
| 코드블록      | \`\`\`python     | `print("Hello")`           | 코드박스                     |
| 인라인 코드    | \`코드\`           | \`a = 3\`                  | `a = 3`                  |
| 구분선       | `---`            | `---`                      | ―――                      |

---

## 🚀Colab 기초

1. Google 계정으로 로그인
2. [https://colab.research.google.com](https://colab.research.google.com) 접속
3. 새 노트북 만들기 또는 Drive에서 열기
4. 파이썬 코드를 작성하여 바로 실행!

---

### 🧾 3. 자주 사용하는 Colab 기능 정리

| 기능           | 설명                                          | 예시 코드 또는 단축키                    |
|----------------|-----------------------------------------------|------------------------------------------|
| 코드 실행      | 셀을 실행                                      | `Shift + Enter`                          |
| 마크다운 작성  | 텍스트 설명, 제목, 수식 등                    | 셀 유형을 "텍스트"로 변경                |
| 셀 추가        | 위/아래 셀 추가                                | `+ 코드`, `+ 텍스트` 버튼 또는 단축키    |
| 파일 업로드    | 로컬 파일을 코랩에 업로드                     | `from google.colab import files`         |
| 구글 드라이브 연동 | 드라이브 파일 접근                              | `from google.colab import drive`         |
| GPU 사용       | 런타임 > 런타임 유형 변경 > 하드웨어 가속기 선택 | GPU / TPU 선택 가능                      |
| 라이브러리 설치 | `pip install` 사용 가능                        | `!pip install pandas`                    |
| 시스템 명령어  | `!`, `%`로 명령어 실행                         | `!ls`, `%timeit`, `!pip list`            |

---

### 🎯 4. Colab 단축키 모음

| 단축키 | 기능            |
|--------|-----------------|
| `Ctrl + M + B` | 아래에 셀 추가 |
| `Ctrl + M + A` | 위에 셀 추가   |
| `Ctrl + M + D` | 셀 삭제        |
| `Ctrl + M + C` | 셀 복사        |
| `Ctrl + M + V` | 셀 붙여넣기    |
| `Ctrl + Enter` | 셀 실행        |
| `Shift + Enter` | 셀 실행 후 다음으로 이동 |

---
