## 📂 프로젝트 초기 설정
### 📍 프로젝트 가져오기
##### - clone 하기
```bash
$ git clone https://github.com/PetGoorm/petgoorm.git
```
<br/>

### 📍 Git remote
##### - 원격 저장소를 관리할 수 있는 명령어
한번만 수행하면 됨!

- clone 한 저장소에 원격 저장소 설정하기
- 원격 저장소 git 주소는 PR을 보낼 저장소
- 원격 저장소 이름은 upstream으로 설정

```bash
$ git remote add upstream https://github.com/PetGoorm/petgoorm.git
```
<br/>

##### - 설정 확인
```bash
$ git remote -v
```
<img src="https://user-images.githubusercontent.com/54580802/209032798-12f3e9b3-2311-4899-b9ac-a841d21e395f.png"  width="400" height="100">

***

## 📂 프로젝트 업로드 순서
### ❗ 꼭 ❗ 
- fork한 저장소를 원격 저장소의 최신 커밋으로 `fetch & merge` 하고 나서 Pull Request 보내기
<br/>

### 🔸 업로드 순서
1. 자신의 Branch를 생성하고, 본인의 Branch에서 기능 구현
2. remote 되어 있나 확인하기
3. fetch & merge 하기
4. commit 하기
5. push 하기
5-5. PR 보내기 전에 fetch & merge 하기
6. PR양식에 맞게 Pull Request 보내기
<br/>

##### 1. Branch 생성하여 작업 진행
- 브랜치 생성
```bash
$ git branch 브랜치이름
```
- 브랜치 변경
```bash
$ git checkout 브랜치이름
```
<img src="https://user-images.githubusercontent.com/54580802/209039154-0e54036b-a1b5-47d0-b9e0-c1f4e2f15e0a.png"  width="400" height="100">
<br/>

##### 2. remote 되어 있나 확인하기
<br/>

##### 3. fetch & merge 하기
###### - fetch
- upstream이라는 이름의 저장소에서 main 브랜치를 가져옴으로써 최신 커밋 내역이 가져옴
```bash
$ git fetch upstream
```
###### - merge
- upstream/master에는 최신 commit 내역이 반영되어 있다.
- 이 반영사항을 내 local 저장소에 반영하려면 merge를 통해 현재 내 main 브랜치에 병합
```bash
$ git merge upstream/main
```
<br/>

##### 4. 코드 수정 후 commit
- 코드를 수정한 후 `git add & commit`
- add 에서 특정 파일만 올리고 싶다면 . 대신 파일명 작성
```bash
$ git add .
$ git commit -m "커밋 메시지"
```
<img src="https://user-images.githubusercontent.com/54580802/209042014-7ae7c43b-85f7-4301-9596-40c76d064e8f.png"  width="400" height="100">

<br/>

##### 5. push 하기
- 현재 branch에서, fork해 온 내 저장소에 push
```bash
$ git push origin 브랜치명
```
<img src="https://user-images.githubusercontent.com/54580802/209046578-a0d1c9ee-9924-4f44-9fa7-0947467fe0a2.png"  width="290" height="100">
<br/>

##### 6. Pull Request 보내기
- github에서 fork해 온 저장소를 들어가서 `Compare & pull request` 버튼 누르기
<img src="https://user-images.githubusercontent.com/54580802/209047527-1a56c9ad-6290-4007-b932-17176e5c220c.png"  width="400" height="150">
<br/>

- PR 양식대로 내용을 작성하고 `Create pull request` 버튼을 눌러 PR 보내기
<img src="https://user-images.githubusercontent.com/54580802/209064175-ab4a0216-ffc7-4d9f-a89b-bf91fe7a3f0e.png"  width="400" height="220">
<br/>
- 원본 저장소에서 PR이 승인되면 merge 성공
<img src="https://user-images.githubusercontent.com/54580802/209063122-61934152-21ef-43dd-96a3-8fba26992d9d.png"  width="350" height="200">