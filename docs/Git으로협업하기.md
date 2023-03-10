## ๐ ํ๋ก์ ํธ ์ด๊ธฐ ์ค์ 
### ๐ ํ๋ก์ ํธ ๊ฐ์ ธ์ค๊ธฐ
##### - clone ํ๊ธฐ
```bash
$ git clone https://github.com/PetGoorm/petgoorm.git
```
<br/>

### ๐ Git remote
##### - ์๊ฒฉ ์ ์ฅ์๋ฅผ ๊ด๋ฆฌํ  ์ ์๋ ๋ช๋ น์ด
ํ๋ฒ๋ง ์ํํ๋ฉด ๋จ!

- clone ํ ์ ์ฅ์์ ์๊ฒฉ ์ ์ฅ์ ์ค์ ํ๊ธฐ
- ์๊ฒฉ ์ ์ฅ์ git ์ฃผ์๋ PR์ ๋ณด๋ผ ์ ์ฅ์
- ์๊ฒฉ ์ ์ฅ์ ์ด๋ฆ์ upstream์ผ๋ก ์ค์ 

```bash
$ git remote add upstream https://github.com/PetGoorm/petgoorm.git
```
<br/>

##### - ์ค์  ํ์ธ
```bash
$ git remote -v
```
<img src="https://user-images.githubusercontent.com/54580802/209032798-12f3e9b3-2311-4899-b9ac-a841d21e395f.png"  width="400" height="100">

***

## ๐ ํ๋ก์ ํธ ์๋ก๋ ์์
### โ ๊ผญ โ 
- forkํ ์ ์ฅ์๋ฅผ ์๊ฒฉ ์ ์ฅ์์ ์ต์  ์ปค๋ฐ์ผ๋ก `fetch & merge` ํ๊ณ  ๋์ Pull Request ๋ณด๋ด๊ธฐ
<br/>

### ๐ธ ์๋ก๋ ์์
1. ์์ ์ Branch๋ฅผ ์์ฑํ๊ณ , ๋ณธ์ธ์ Branch์์ ๊ธฐ๋ฅ ๊ตฌํ
2. remote ๋์ด ์๋ ํ์ธํ๊ธฐ
3. fetch & merge ํ๊ธฐ
4. commit ํ๊ธฐ
5. push ํ๊ธฐ
5-5. PR ๋ณด๋ด๊ธฐ ์ ์ fetch & merge ํ๊ธฐ
6. PR์์์ ๋ง๊ฒ Pull Request ๋ณด๋ด๊ธฐ
<br/>

##### 1. Branch ์์ฑํ์ฌ ์์ ์งํ
- ๋ธ๋์น ์์ฑ
```bash
$ git branch ๋ธ๋์น์ด๋ฆ
```
- ๋ธ๋์น ๋ณ๊ฒฝ
```bash
$ git checkout ๋ธ๋์น์ด๋ฆ
```
<img src="https://user-images.githubusercontent.com/54580802/209039154-0e54036b-a1b5-47d0-b9e0-c1f4e2f15e0a.png"  width="400" height="100">
<br/>

##### 2. remote ๋์ด ์๋ ํ์ธํ๊ธฐ
<br/>

##### 3. fetch & merge ํ๊ธฐ
###### - fetch
- upstream์ด๋ผ๋ ์ด๋ฆ์ ์ ์ฅ์์์ main ๋ธ๋์น๋ฅผ ๊ฐ์ ธ์ด์ผ๋ก์จ ์ต์  ์ปค๋ฐ ๋ด์ญ์ด ๊ฐ์ ธ์ด
```bash
$ git fetch upstream
```
###### - merge
- upstream/master์๋ ์ต์  commit ๋ด์ญ์ด ๋ฐ์๋์ด ์๋ค.
- ์ด ๋ฐ์์ฌํญ์ ๋ด local ์ ์ฅ์์ ๋ฐ์ํ๋ ค๋ฉด merge๋ฅผ ํตํด ํ์ฌ ๋ด main ๋ธ๋์น์ ๋ณํฉ
```bash
$ git merge upstream/main
```
<br/>

##### 4. ์ฝ๋ ์์  ํ commit
- ์ฝ๋๋ฅผ ์์ ํ ํ `git add & commit`
- add ์์ ํน์  ํ์ผ๋ง ์ฌ๋ฆฌ๊ณ  ์ถ๋ค๋ฉด . ๋์  ํ์ผ๋ช ์์ฑ
```bash
$ git add .
$ git commit -m "์ปค๋ฐ ๋ฉ์์ง"
```
<img src="https://user-images.githubusercontent.com/54580802/209042014-7ae7c43b-85f7-4301-9596-40c76d064e8f.png"  width="400" height="100">

<br/>

##### 5. push ํ๊ธฐ
- ํ์ฌ branch์์, forkํด ์จ ๋ด ์ ์ฅ์์ push
```bash
$ git push origin ๋ธ๋์น๋ช
```
<img src="https://user-images.githubusercontent.com/54580802/209046578-a0d1c9ee-9924-4f44-9fa7-0947467fe0a2.png"  width="290" height="100">
<br/>

##### 6. Pull Request ๋ณด๋ด๊ธฐ
- github์์ forkํด ์จ ์ ์ฅ์๋ฅผ ๋ค์ด๊ฐ์ `Compare & pull request` ๋ฒํผ ๋๋ฅด๊ธฐ
<img src="https://user-images.githubusercontent.com/54580802/209047527-1a56c9ad-6290-4007-b932-17176e5c220c.png"  width="400" height="150">
<br/>

- PR ์์๋๋ก ๋ด์ฉ์ ์์ฑํ๊ณ  `Create pull request` ๋ฒํผ์ ๋๋ฌ PR ๋ณด๋ด๊ธฐ
<img src="https://user-images.githubusercontent.com/54580802/209064175-ab4a0216-ffc7-4d9f-a89b-bf91fe7a3f0e.png"  width="400" height="220">
<br/>
- ์๋ณธ ์ ์ฅ์์์ PR์ด ์น์ธ๋๋ฉด merge ์ฑ๊ณต
<img src="https://user-images.githubusercontent.com/54580802/209063122-61934152-21ef-43dd-96a3-8fba26992d9d.png"  width="350" height="200">