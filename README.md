
# Git Guide
git을 사용하면서 자주 사용하는 명령어를 정리. (맨날 까먹고 검색하는 나를 위해서)
---
## 기본설정
### git init
	$ git init
최초로 git 설정을 할 때 사용하는 명령어로, `.git` 폴더가 생성된다. `.git` 폴더는 숨겨져 있음. 이 폴더를 지우면 모든 것이 사라진다. 만약에 그동안 관리한걸 다 날리고 싶으면 쿨하게 삭제하면 된다.

### git status
	$ git status
현재 폴더의 상태를 나타내주는 명령어. add나 commit 되지 않은 파일 등을 표시해주고, 커밋 상태 등 여러 가지 정보를 보여준다. 종종 사용함.

### git config
	$ git config --global user.name "cutelee"
	$ git config --global user.email "cutelee2@khu.ac.kr"
git config에 **--system** 옵션을 주면 `/etc/gitconfig` 파일을 찾으며, 이 파일의 설정은 모든 사용자와 모든 저장소에 적용된다. **--global** 옵션을 주면 `~/.gitconfig` 파일을 찾으며 이 설정은 해당 저장소에만 적용되는 설정이다. 설정파일을 직접 수정해도 되지만, git config 명령어를 사용하는 것이 더 편리.
---
## Commit
	$ git commit -m "[contents]"
현재 add된 파일들을 커밋해주며, contents에는 커밋메세지를 작성하면 된다.
---
## 원격 저장소
### git clone
	$ git clone [원격저장소 주소]
해당 원격저장소 주소의 파일을 받아오는 명령어.

### git remote
	$ git remote -v
단축이름, 연결된 원격저장소 url을 보여주는 명령어. -v 옵션이 없으면 단축이름만 알려준다.

	$ git remote add [name] [url]
name으로 단축이름을 설정하고, url을 연결해주는 명령어.

	$ git remote set-url [name] [url]
name에 연결된 url을 url로 바꿔주는 명령어.

### git push
	$ git push [name] master
name에 연결되어 있는 원격저장소로 현재 상태를 전송해주는 명령어.
---
