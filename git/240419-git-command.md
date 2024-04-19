# 202419 Git 수업 최우영 강사님

## git config

```shell
git config [--global] user.name "{username}"
git config [--global] user.email "{emailaddr}"
git config [--global] core.editor "vim"
git config [--global] core.pager "cat"
```

~/.gitconfig, .git/config 파일을 직접 수정할 수도 있음.

### --global 이 있는 경우

1. 전체 저장소에 영향을 줌.

2. ~/.gitconfig 파일에 저장됨.

### --global 이 없는 경우

1. 해당 저장소에만 영향을 줌.

2. .git/config 파일에 저장됨.

3. global 값보다 우선

### git config --list

config 키값 목록 출력

동일한 키값에 대해 global, local? 키값이 설정되어 있다면

2개 노출 될 수 있음. 아래 쪽이 local? 키값인듯하며 아래 쪽 키값이 위쪽 키값을 오버라이드 하는듯.

user.name 은 깃허브 유저 이름 입력.

user.email 은 깃허브 이메일 입력.

## git alias lg

위 제목을 구글링하면 아래와 같은 alias 를 찾을 수 있음.

```shell
git config --global alias.lg "log --graph --pretty=tformat:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --decorate=full"
```

git lg 로 사용하며, git log 보다 좀더 보기좋다.


## git 저장소를 깃허브에서 먼저 만들기 vs PC 에서 git init 하기

일반적으로 깃허브에서 저장소를 만든 후, PC 에서 git clone 을 하는 방법을 사용함.

PC 에서 git init 을 하면, 브랜치 이름이 master 로 되어 있기 때문에 main 으로 브랜치 이름을 수동으로 바꿔주는 번거로움도 있음.


## 깃허브에서 저장소 만들때 주의할 점

Private 으로 만들면 Pro 버전이 아니고서야 기능이 몇개 막힘.

README.md 생성에 체크.

가장 자유로운 라이센스는 "MIT License". 제약사항이 없다.

가장 유의 해야하는게 GPL 라이센스..

- 요게 붙은 소스를 갖다 쓴 순간, 우리 프로젝트는 오픈소스가 되어야 한다! 꼭 확인하라!

## commit 은 동작하는 최소 단위로 올려야함.

메소드 하나하나를 별도의 커밋으로 커밋하라.

## 커밋은 "제목" 과 "내용" 으로 구성

제목과 내용 사이에 1줄의 빈줄이 있어야 함.

제목은 영어로 작성.

## Personal access token

이것 없어도 깃허브에 push 잘 됬었음.

정확히 언제 필요할까?

## Conventional Commits

https://www.conventionalcommits.org/ko/v1.0.0/

코드를 보지 않더라도, 제목과 내용만 보더라도 해당 커밋이 뭘 했는지 이해 될 수 있도록 작성.

## README.md

https://github.com/tiangolo/fastapi 참고

템플릿을 지킬것.

## .gitignore

https://gitignore.io/

프로젝트 시작할때 추가하자.

## .ipynb

프로필 사진 클릭 -> Feature preview -> Rich Jupyter Notebook Diffs 를 Enable 로 변경.

.ipynb 파일을 비교하기 좋게 보여줌.

## GitHub Blog

깃허브에서 저장소 생성시, 저장소 이름을 username.github.io 로 생성하면,

https://username.github.io 로 웹 호스팅 가능.

정적 페이지를 생성해주는 도구를 사용.

- hexo

