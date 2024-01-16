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
2. 수정한 .md 파일은 main branch에 pull requests 하기
   * 파일 업로드로 하시는게 가장 편할 듯 합니다.

[MyST로 내 문서 화려하게 꾸미는 방법](https://jupyterbook.org/en/stable/reference/cheatsheet.html)
