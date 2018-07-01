tail -f log |

grep -line-buffred Error > error.txt

### 리눅스 메뉴얼 rtfm

- man : 예제..

- bashSehll -> zsh 로 변경

- ssh : 접속, scp : 동기..(ssh로 접속해서 복사?), sftp

- rsyslog : system log 변경

- cron : 반복작업

- vim/emacs : emacs 별도 설치 필요.....

vim plugin 사용법 필수 (auto comflit)

- 

git 특징 : branch

tmux : background에서 다른 프로그램을 실행 시킬 수 있다.

upstart : 시작프로그램 작업시

systemd :

 syntax highlighting

 #터미널 경로 짧게 표시하기
 .bashrc 파일에서 아래 \w 를 \W 로 바꾸고, source .bashrc를 한다.

if [ "$color_prompt" = yes ]; then
    PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '
else
    PS1='${debian_chroot:+($debian_chroot)}\u@\h:\w\$ '

fi

이렇게 수정,
=> PS1='${debian_chroot:+($debian_chroot)}\u@\h:\W\$ '

## 찾기
find ~ -type f -exec grep "찾을문자" {} \; -print

##연결프로그램 설정
-$HOME/.local/share/applications/mimeapps.list 

-1. 우선 /etc/gnome/default.list을 찾아봅니다. 거기에 해당 MIME 타입에 기술된 프로그램 목록을 읽습니다.
-2. 그 다음 ~/.local/share/applications/mimeapps.list를 찾아봅니다. 여기에 있는 설정이 /etc/gnome/default.list보다 우선합니다.
-3. (이건 추측입니다)그래도 해당 안되는 것은, MIME이 text/* 일 때 /usr/bin/gnome-text-editor를 실행합니다. (/usr/bin/editor도 있는데 이건 터미널에서 실행할 때 해당됩니다.)