# 프로그래머스 1일차 과제
---

### `CLI`만 활용하여 `GitHub`에 업로드하기

1. [GitHub](https://github.com) 웹사이트 접속
2. 상단 메뉴에서 **Repositories** -> **New** 클릭
3. 저장소 이름 입력 (예: `test-project`)
4. ✅ 아래 옵션은 **선택하지 않음**
   - Add a README file ❌
   - Add .gitignore ❌
   - Choose a license ❌
5. **Create repository** 버튼 클릭
6. 생성된 저장소 페이지의 주소(URL)를 복사해둡니다!
   예: `https://github.com/사용자이름/test-project.git`
---

#### 1. Git 초기화
먼저 프로젝트 폴더로 이동하고 Git 저장소를 초기화 합니다.

```bash
cd 프로젝트_폴더명 (cd는 해당 폴더 위치로 이동 명령어)
    | 터미널에서 git init으로 초기화
```

---

#### 2. 파일 추가 및 커밋

```bash
git add . (모든 수정 파일 스테이징에 올리는 명령어)
git commit -m '커밋하는 파일 설명' (스테이징 상태의 파일 커밋)
    or
git commit -am '커밋하는 파일 설명' (스테이징과 커밋을 동시에 하는 명령어)
```

---

#### 3. 원격 저장소(origin) 연결

```bash
git remote add origin `https://github.com/사용자이름/test-project.git`
- 원격 저장소 연결은 GitHub에 프로젝트를 올릴 때 한 번만 remote 추가하면 됨
```
###### ✅ 참고: git remote -v 명령어로 연결 확인 가능

---

#### 4. GitHub로 푸시 (업로드)
```bash
git push -u origin main
```
###### ※ main 대신 master일 수도 있습니다. git branch로 확인하세요.

---

#### 5. 이후 업데이트할 때
변경 사항을 반영할 때는 아래 명령어만 입력해주시면 됩니다.
```bash
git add .
git commit -m "메시지"
git push
```

---

#### 🧠 팁
```bash
git status
    - Git 상태 확인
git branch
    - 현재 브랜치 확인
git log --oneline
    -  커밋 로그 확인
```