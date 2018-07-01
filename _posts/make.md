##MakeFile
- 변경된 소스에 대해서만 Objet를 만들고자 할 경우
- gcc 사용 시 변경에 상관 없이 컴파일, 또는 링크
- gcc -c : 컴파일 -> .o
- gcc -o : 링크 -> 실행파일

###구조
- 만들어질 것 : 필요한것
        실행 명령
        실행 명령
- 만들어질 것 : 필요한것.
        실행 명령
[ex]
hello : hello.o main.o
        gcc -o hello hello.o mian.o
hello.o : hello.c
        gcc -c hello.c

main.o : main.c hello.h
        gcc -c main.o

- MakeFile는 시간에 따른 변경 여부를 정한다.
- CFLAGS = c언어 컴파일 옵션..
- 동적변경 - make CFLAGS=-std=c11

- $@ : TagetName
- $< : 정의된 목록의 첫번째