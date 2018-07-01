### Vim with Ubuntu

## Ubuntu 
#https://www.vim.org/download.php
- 주의 (기본 설치된 vi는 키 사용의 어려움)

#설치
- sudo apt-get install vim
#제거
- sudo apt-get remove vim
#설치경로
- /usr/share/vim/vim80
#skin 변경 (colors에 skin파일 삽입)
- /usr/share/vim/vim80/colors
- .vimrc 수정
>> colorscheme 스킨명

#Vim Mode
- ESC : Normal Mode 
- a : 한칸뒤로 입력, A : 
- i : 현재 위치 입력, I : 맨 처음
- o : 행의 아래, O : 행의 윈에 빈행
- R :  수정 모드 
- w : 단어간 이동 , W : 단어간 이동(,. 무시)
- b : 단어끝 이동 
- $ : 행의 처음
- ^ : 행의 시작
- gg : 맨앞
- G : 맨뒤
- Ctrl+F : 페이지 아래
- Ctrl+B : 페이이 위
- yy : 행 복사, 5yy : 5줄 복사
- p : 붙여넣기
- x : 뒷문자, X: 앞문자 (숫자 조합 5x : 5자 지움) 삭제
- D : 한 줄 잘라내기(줄 변경 없음)
- dd : 한 줄 잘라내기
- u : undo (normal mode)
- Ctrl + R : redo
- / : 문자열 검색
- [range]s/찾을 문자열/교체할 문자열/ 옵션
>> :1,$/s/a/i/g == :1,$s,a,i,g
>> 옵션 : g (모든 문자열), i(대소문자를 무시), c(확인), e(에러 무시)
- 외부 url 내용 복사 붙여넣기
>> :r !curl --silent 주소
- tail 

- http://www.openvim.com/
- http://vim-adventures.com/
- https://danielmiessler.com/study/vim

- https://www.fprintf.net.vimCheatSheet.html
- http://freestrokes.tistory.com/entry/Ubuntu-vi-%EC%97%90%EB%94%94%ED%84%B0-%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0
