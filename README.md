## Clone this repository
test-page 브랜치만 clone 합니다
```bash
git clone --branch test-page https://github.com/DCV1/tutorial.git
```

## Install packages
You can install Jupyter Book [via `pip`](https://pip.pypa.io/en/stable/):

```bash
cd tutorial
pip install requirements.txt
```
## Build
```bash
cd ../
jupyter-book build tutorial
```
## Markdown 업로드 방법
1. 로컬에서 build가 잘 되었는지 로컬 호스트에서 확인하기
   ```bash
   python -m http.server 8080
   ```
2. 각자 local에서 feature 브랜치 만들기
   ```bash
   git checkout -b feature-01
   ```
3. feature 브랜치의 commits를 origin(원격 저장소)으로 업로드하기
   ```bash
   git push origin feature-01 
   ```
4. feature 브랜치는 upstream하여 계속 작업하기
   ```bash
   git branch --set-upstream-to origin/feature-01
   ```
5. 작업한 내용은 develop 브랜치로 pull requests

[MyST로 내 문서 화려하게 꾸미는 방법](https://jupyterbook.org/en/stable/reference/cheatsheet.html)
