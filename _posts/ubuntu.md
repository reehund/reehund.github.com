### Ubuntu 18.04 설치

## Oracle VM VirtualBox 설치
1. 가상머신(VBOX) 호스트키 변경
- 부모 플랫폼으로 포커스를 이동하기 위한 키 (기본 우측 Ctrl) 
- VBOX 파일-> 환경설정(Ctrl + G)-> 입력 -> 가상머신 탭 -> 호스트 키 조합 변경
2. 가상 머신 만들기
- 종류 : Linux 
- 버전 : Ubuntu (64-bit) 
- 메모리 : 2048MB (추천 1024MB)
- 용량 : 10.0GB (추천 10.0GB)
3. 시동디스크 파일 선택 (iso 파일)
- https://www.ubuntu.com/download/desktop

4. root 계정 활성화
- sudo su - root
- 비번지정
- sudo passwd root 

5. 자동 로그인시 root 계정으로 (이하버전)
- gedit /etc/lightdn/lightdn.conf
>> autologin-user=root 변경
- gedit /root/.porfile
>> mesg n || true 주석
- vim /usr/share/lightdm/lightdm.conf.d/50-ubuntu.conf
>>greeter-show-manual-login=true
>>재부팅

6. 18.04 자동 로그인
- sudo passwd root
- vim /etc/pam.d/gdm-password
>>#%PAM-1.0
>>auth    requisite       pam_nologin.so
>>#auth   required        pam_succeed_if.so user != root quiet_success
- vim /etc/pam.d/gdm-autologin
>>#%PAM-1.0
>>auth    requisite       pam_nologin.so
>>#auth   required        pam_succeed_if.so user != root quiet_success
- vim /etc/gdm3/custom.conf 
>>[daemon]
>>AutomaticLoginEnable=true
>>AutomaticLogin=root
>>...
>>[security]
>>AllowRoot=true
-재부팅 후 /root/.profile 변경
>>tty -s && mesg n || true

7. 방화벽 활성화
-ufw enable

8. 끄기
halt -p