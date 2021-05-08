> ## Git & Github
컴퓨터학부 20201816 강병민 <br>
https://github.com/kbn3751/GitGithub

---

## **1. git** 
 - Git은 고급 작업과 내부에 대한 전체 액세스를 모두 제공하는 비정상적으로 풍부한 명령 세트를 갖춘 빠르고 확장 가능한 분산 개정 제어 시스템입니다.

 <br>

 ## **2. git 명령어**
  오늘 소개할 git의 명령어들은 다음과 같습니다.
 - [init](##init)
 - [config](##config)
 - [status](##status)
 - [add](##add)
 - [commit](##commit)
 - [log](##log)
 - [reset--hard](##reset--hard)
 - [branch](##branch)
 - [checkout](##checkout)
 - [merge](##merge)
 - [rebase](##rebase)
 - [remote](##remote)
 - [push](##push)
 - [clone](##clone)
 - [pull](##pull)
 - [tag](##tag)

 ---

  ## init
    1) 일단 프로젝트를 수행할 폴더와 markdown(이후 md)파일을 만들어야 합니다.
    2) 현재 만든 빈 폴더(이름 : project)를 git bash를 이용하여 불러왔습니다. 그런 다음 프로젝트를 진행할 md파일이 만들어진 상태입니다.
    3) 이제 git 저장소를 만들어 git을 사용해보려 합니다.
    4) 그러기 위해서는 git init라는 명령어를 사용합니다.
    5) 이 명령은 .git 이라는 하위 디렉토리를 만듭니다. 즉, 새로 만든 빈 폴더가 git의 관리하에 들어갔다는 의미입니다. 이렇게 git init 명령어를 실행하게 되면 폴더에 .git으로 숨겨진 폴더가 생기게 되는데 .git 디렉토리에는 저장소에 필요한 뼈대 파일(Skeleton)이 들어 있다. 한 가지 알아야 할 점은 이 명령만으로는 아직 프로젝트의 어떤 파일도 관리하지 않는다

> $ git init
    
![gitinit](https://ifh.cc/g/1xq8kk.png)

---

## config
    1) 현재 init 명령어로 뼈대 파일을 만든 상태입니다.
    2) git을 사용하기 위해서는 초기 설정을 해줘야 합니다. 대표적으로 사용자의 이름과 이메일 주소를 설정하고 확인하고자 합니다.
    3) 이를 위해 git config 명령어를 사용해야 합니다.
    4) 따라서 config 명령어를 통해 사용자의 정보를 입력받고 그것이 잘 입력되었는지 확인이 가능합니다.
    5) 이 명령어는 'config--global'을 자주 사용하는데 특정 사용자(즉 현재 사용자)에게만 적용되는 설정입니다. 이 옵션으로 이 파일을 읽고 쓸 수 있습니다.--global 옵션으로 설정하는 것은 딱 한 번만 하면 됩니다. 만약 프로젝트마다 다른 이름과 이메일 주소를 사용하고 싶으면 --global 옵션을 빼고 명령을 실행하면 됩니다.

>$ git config --global user.name "KBM" <br>
>$ git config --global user.email "kbn3751@naver.com" <br>
>$ git config --global user.name <br>
>$ git congif --global user.email

![gitconfig](https://ifh.cc/g/xR27AA.png)

---

## status
    1) 현재 git init으로 .git이라는 하위 디렉토리를 만든 상태입니다.
    2) 현재 자신의 상태를 확인해보고 싶습니다.
    3) 이를 위해 git status를 사용하면 됩니다.
    4) git status는 현재 사용 중인 프로젝트의 상태를 알려주는 목적으로 사용되고 있습니다. 빨간색 글씨는 아직 untracked(관리대상 아님)되어 있거나 변경사항이 있는 경우 뜨게 됩니다.

> $ git status

![gitstatus](https://ifh.cc/g/2phGQ9.png)

---

## add

    1. 현재 git status로 markdown.md파일이 untracked 상태임을 확인하였습니다. 즉 git에서 아직 보고있지 않은 상태를 뜻합니다. 또한, 빨간색으로 표시된 것은 markdown.md 파일들이 만들어졌다는 사실을 의미합니다.
    2. 지금까지 작성한 내용들을 저장하고자 합니다.
    3. 이럴 경우엔 git add 명령어를 사용하면 됩니다.
    4. 따라서 git add를 사용하여 새로운 파일이나 기존 파일의 수정사항을 커밋 명령을 실행 전 추가할 수 있습니다. git status 명령을 다시 실행하면 markdown.md파일이 Tracked 상태이면서 커밋에 추가될 Staged 상태라는 것을 확인할 수 있다.
    5. git add에서 자주 사용 할 옵션으로는 git add -A이나 git add *가 있습니다.  -A는 모든 파일을 add하는 것이고, *는 뒤에 파일 형태를 쓰게 되면 적은 파일 형태의 모든 파일이 add가 됩니다.

> $ git add markdown.md <br>
> $ git add -A <br>
> $ git add *.md

![gitadd](https://ifh.cc/g/kLTn6r.png)

---

## commit

    1. 현재 git add를 통해 Staged 상태, 즉 git의 타임캡슐에 넣은 상태입니다.
    2. 이 Staged 상태를 저장하고자 합니다. 다른 말로 이 git의 타임캡슐을 완전히 묻어 버려 저장하고자 합니다.
    3. 이럴 경우 git commit 명령어를 사용하면 됩니다.
    4. 따라서 이 명령어는 git add로 저장된 부분들을 완전히 저장시키는 역할을 수행합니다. 즉, add는 타임캡슐에 넣는 행위이고 commit은 그 타임캡슐을 묻는 다고 생각하시면 됩니다. 
    5. git commit에 주로 사용되는 옵션은 git commit -m ""입니다. 파일을 commit할때 그냥 실행하게 되면 나중에 어떤 내용인지 바로 알 수 없기에 이 옵션을 사용하게 되면 이 캡슐의 설명을 간략하게 적을 수 있습니다.

> $ git commit <br>
> $ git commit -m "first commit"

![gitcommit](https://ifh.cc/g/WGQwPb.png)

---

## log

    1. 현재 git commit으로 파일을 완전히 저장한 상태입니다.
    2. 아직 한 가지만 commit한 상태이지만 제대로 되었는지 확인하고자 합니다.
    3. 이럴 경우엔 git log를 사용하면 됩니다.
    4. 따라서 git log는 이제까지 저장된 저장소의 commit history를 작정자와 시간을 시간순으로 확인해 볼 수 있는 기능을 가지고 있습니다.
    5. git log에 자주 사용하는 옵션은 '-p', '--graph --all --decorate'가 있습니다. 이 git log -p -2의 -p는 각 commit의 diff 결과를 보여주고, '--graph --all --decorate'는 시각화된 다른 branch들의 작업내역을 볼 수 있습니다. 

> $ git log <br>
> $ git log -p -2 <br>
> $ git log --graph --all --decorate

![gitlog](https://ifh.cc/g/YiHIF3.png)

---

## reset--hard

    1. 현재까지의 문서를 add로 staging area에 옮겨 commit한 상태에서 계속해서 문서를 추가하여 add와 commit을 반복하는 상황입니다.
    2. 새로 추가한 내용이 마음에 들지 않아 이전 버전으로 수정하고자 합니다.
    3. 이럴 경우엔 git reset --hard를 사용하면 됩니다.
    4. 이 git reset --hard의 경우에는 git log를 통해 돌아가고자 하는 시점의 commit 일련번호 앞 6글자를 복사하여 git reset과 --hard 사이에 넣게 되면 원하는 시점으로 돌아가게 됩니다.
    5. git reset에 자주 사용하는 옵션은 위에서도 언급했듯이 --hard를 자주 사용합니다. git reset 일련번호6자리 --hard를 통해 원하는 시점으로 되돌아 갈 수 있습니다.

> $ git reset 일련번호6자리 --hard

![gitreset](https://ifh.cc/g/IU6LDn.png) 

---

## branch

    1. 현재 master란 하나의 환경안에서 markdown.md 파일안의 내용을 계속해서 추가하여 add 및 commit을 반복하고 있는 상태입니다.
    2. 새로운 시도를 해보고자 하는데 기존의 파일을 수정해보는 시도를 해보고 싶지만 쉽게 건드리지 못할 때 새로운 시도를 해볼 수 있는 평행우주를 만들어 보고자 합니다.
    3. 이럴 경우엔 git branch 란 명령어를 사용하면 됩니다.
    4. branch는 가지치기라고 생각하면 됩니다. git brance를 통해 master란 기존 branch 대신 평행 우주공간을 만들수 있습니다. 새로 만들어진 branch는 기존의 master의 상태를 그대로 가져오게 됩니다. 이 공간에서 다양한 시도를 해볼 수 있습니다.
    5. git branch에서 자주 사용하는 옵션은 '-v', '-D'가 있습니다. git branch -v는 마지막 commit 메시지도 함께 보여줍니다. git branch -D는 다 쓴 branch를 삭제하는 기능을 가지고 있습니다.

> $ git branch 이름 <br>
> $ git branch -v <br>
> $ git branch -D 이름

![gitbranch](https://ifh.cc/g/QzLns4.png)

---

## checkout

    1. git branch로 기존 master에서 평행우주가 만들어진 상태입니다.
    2. 만들어진 평행우주로 이동하고자 합니다.
    3. 이럴 경우에는 git checkout 명령어를 사용하면 됩니다.
    4. git checkout 명령어는 checkout뒤에 저장공간의 이름을 쓰게 되면 작성된 이름의 공간으로 이동하게 됩니다. 이동하게 되면 평행우주에서 작성된 내용은 기존 master branch로 이동되지는 않습니다.
    5. git checkout에 자주 사용하는 옵션은 '-b'가 있습니다. git checkout -b 이름을 작성하게 되면 새로운 branch를 만드는 동시에 그쪽으로 이동시켜 줍니다.

> $ git checkout 이름 <br>
> $ git checkout -b 이름 

![gitcheckout](https://ifh.cc/g/F5NobI.png)

---

## merge

    1. git branch로 여러 branch를 만들어 놓고 각각의 branch에서 시도를 해보는 상황입니다.
    2. master branch에 나머지 branch의 파일을 가져오고자 합니다.
    3. 이런 경우에는 git merge를 사용하시면 됩니다.
    4. 먼저 master branch로 돌아온 이후 git merge 뒤에 변화를 가져 올 branch의 이름을 적게 되면 다른 branch에서 작성된 내용들이 master branch에 모두 적용된 상태로 될 것입니다. 
    5. 만약  master와 다른 branch가 동일한 라인에 동일한 파일을 수정을 했다면 갈등, 충돌이 있다고 경고 메시지가 뜨게 됩니다. 이럴 경우엔 하나를 선택하고 나머지는 수정하면 해결됩니다
    6. git merge에서 자주 사용하는 옵션에는 '--commit'이 있습니다. git merge --commit은 병합을 수행하고 결과를 커밋하는 역할을 수행합니다.

> $ git merge 이름 <br>
> $ git merge --commit 이름

![gitmerge](https://ifh.cc/g/oeEVeB.png)

---

## rebase

    1. git branch로 여러 branch를 만들어 놓고 각각의 branch에서 시도를 해보는 상황입니다.
    2. master branch에 나머지 branch의 파일을 가져오고자 하는데 모든 변경사항을 log로 확인시 한 줄로 깔끔하게 정리해주고자 합니다.
    3. 이럴 경우에는 git rebase 명령어를 사용하면 됩니다.
    4. git rebase 이름 은 git merge와 똑같이 다른 branch(=이름)의 파일들이 옮김을 받는 branch에 옮겨지게 됩니다. 다만 차이점은 git log로 확인 시 merge는 복잡한 반면에 git rebase는 분기들이 한 줄로 깔끔하게 정리된 것을 확인할 수 있습니다. 
    5. git rebase에 자주 사용하는 옵션은 '-i'가 있습니다. git rebase -i는 재기반이 될 커밋 목록을 만듭니다. 사용자가 리베이스하기 전에 해당 목록을 편집하도록 합니다. 이 모드는 커밋을 분할하는 데 사용할 수도 있습니다.

> $ git rebase 이름 <br>
> $ git rebase -i

![gitrebase](https://ifh.cc/g/T1j6q2.png)

---

## remote

    1. 현재 컴퓨터안에서만 git으로 저장 및 관리가 되어 있는 상태입니다.
    2. 이러한 프로젝트를 온라인(Github)에 업로드해서 저장하고자 합니다.
    3. 이럴 경우에는 git remote 명령어를 사용하면 됩니다.
    4. git remote를 사용하기 전 git status로 모두 commit되었는지 확인 후 사용하면 됩니다. 'git remote add origin Github레파지토리.git'을 입력하면 됩니다. 이것의 의미는 이 github 레파지토리를 이 폴더의 'origin'이란 이름의 원격 저장소로 설정하겠다는 의미입니다.
    5. git remote에 자주 사용하는 옵션은 '-v'입니다. git remote -v는 좀 더 자세한 내용과 이름 뒤이 원격 URL을 표시합니다.

> $ git remote add origin https://github.com/kbn3751/GitGithub.git
> $ git remote [-v | --verbose]

![gitremote](https://ifh.cc/g/HeQlOK.png)

---

## push

    1. 위에 git remote를 통해 필자의 github에 원격저장소로 지정만 되어있는 상태입니다.
    2. 자신이 작성한 프로젝트에서 커밋한 내용들을 github 레파지토리에 올리고자 합니다.
    3. 이럴 경우 git push 명령어를 사용하면 됩니다.
    4. 앞서 git remote 명령어를 실행한 후 'git push -u origin master'을 실행하게 되면 자신의 github 레파지토리에 master의 내용이 복사가 됩니다. github에서 확인하면 각 파일이 어떤 commit이 마지막으로 생성되거나 변경된지 알 수 있습니다. 
    5. git push에서 자주 사용하는 옵션은 '-u'입니다. git push -u 는 최신이거나 성공적으로 푸시된 모든 분기에 대해 인수 없는 git pull 및 기타 명령에 사용되는 업스트림(추적) 참조를 추가합니다. 
> $ git push origin master <br>
> $ git push -u origin master

![gitpush](https://ifh.cc/g/XRPn21.png)

---

## clone

    1. git remote 와 git push를 통해 컴퓨터와 온라인 Github가 연결되고 정보를 공유한 상태입니다.
    2. Github에 있는 파일들을 다른 내 컴퓨터에 불러오고자 하는 상태입니다.
    3. 그럴 경우에는 git clone 명령어를 사용하면 됩니다.
    4. git clone 이후에 자신의 GitHub 레파지토리주소.git을 입력하게 되면 레파지토리 명의 폴더가 생기게 됩니다. 이후 이 폴더에서 작업을 하려면 'cd .\폴더명\'을 입력해 폴더 안으로 들어가서 작업을 하시면 됩니다.
    5. git log를 통해 확인해보면 그대로 복사(clone)된 것을 알 수 있습니다.
    6. git clone에서 자주 사용하는 옵션은 '-l'입니다. 'git clone -l'은 복제할 리포지토리가 로컬 컴퓨터에 있는 경우 이 플래그는 일반적인 "Git aware" 전송 메커니즘을 무시하고 개체 아래에 있는 HEAD와 모든 것을 복제하고 디렉토리를 참조합니다.

> git clone https://github.com/kbn3751/GitGithub.git

![gitclone](https://ifh.cc/g/qlDYzq.png)

---

## pull

    1. 여러 컴퓨터에서 하나의 Github에 연결된 상태로 각자 작업을 한 후 Github에 올린 상태입니다.
    2. 새로 추가된 Github의 파일을 자신의 컴퓨터에 옮기고자 합니다.
    3. 그럴 경우에 git pull 명령어를 사용하면 됩니다.
    4. git pull origin(=원격명) master(=branch명)을 입력하게 되면 Github의 파일들을 다운받을 수 있습니다. 뿐만아니라 커밋 내역까지도 다운받아집니다.
    5. git pull에 자주 사용하는 옵션은 '--rebase'입니다. git history를 정리학 ㅣ위해서 자주 사용되는 옵션으로 history가 정리가 된다는 장점이 있지만 별도의 알림없이 영구적으로 history를 임의로 변경시키기 때문에 주의가 필요합니다.

> $ git pull origin master <br>
> $ git pull --rebase

![gitpull](https://ifh.cc/g/Cd3GOd.png)

---

## tag

    1. 프로젝트의 내용을 첨가하여 add와 commit을 반복하고 있는 상태입니다.
    2. 특정 부분의 commit을 표시해두고자 합니다.
    3. 이럴 경우에 git tag 명령어를 사용하면 됩니다.
    4. Git tag는 두 종류가 있습니다.
    5. Annotated Tag : Git 데이터베이스에 태그를 만든 사람의 이름, 이메일과 태그를 만든 날짜, 그리고 태그 메시지도 저장합니다. 'git tag -a 이름'으로 작성하면 됩니다.
    6. Lightweight Tag :기본적으로 파일에 커밋 체크섬을 저장하는 것뿐이다. 다른 정보는 저장하지 않습니다. -a, -s, -m 옵션을 사용하지 않는다. 이름만 달아줄 뿐입니다.
    7. 앞서 언급했듯이 git tag에 자주 사용하는 옵션은 '-a','-m'이 있으며 검색할 때 사용하는 '-l','--list'가 있습니다.

> $ git tag -l "이름" <br>
> $ git tag -a 이름 -m "설명" <br>
> $ git tag 이름

![gittag](https://ifh.cc/g/Je3cBt.png)

<br>

---

<br>

## 결과
|[add](##add)|[branch](##branch)|[checkout](##checkout)|[clone](##clone)|[commit](##commit)|[config](##config)|[init](##init)|[log](##log)|
|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
|  O  |  O  |  O  |  O  |  O  |  O  |  O  |  O  |

|[merge](##merge)|[pull](##pull)|[push](##push)|[rebase](##rebase)|[remote](##remote)|[reset--hard](##reset--hard)|[status](##status)|[tag](##tag)|
|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
|  O  |  O  |  O  |  O  |  O  |  O  |  O  |  O  |
