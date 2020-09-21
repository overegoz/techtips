# SSH 사용

## Terminal emulator
- PuTTY 
  - 공식 홈 : https://www.putty.org/
  - 다운로드 페이지 : https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html
  - Alternative binary files 중에서 다운받기 (설치 불필요)
  
##  Ubuntu : SSH 서버 설치
  - sudo apt update
  - sudo apt install openssh-server
  - SSH 서버 설정파일 : /etc/ssh/sshd_config
  - systemctl status ssh // ssh 서비스가 동작 중인지를 확인
  
## SSH 접속 허용, 거부, IP 대역
  - /etc/hosts.allow 에는 접속 가능한 IP 대역을
  - /etc/hosts.deny 에는 접속 거부할 IP 대역을 입력
  - sudo systemctl restart ssh // ssh 서비스 재시작
  
## ssh-key로 접속하기
  - 서버 컴퓨터 S, 클라이언트 컴퓨터 C
  - S에서 SSH 설정파일을 열고, "PubkeyAuthentication"을 "yes"로 설정 후, ssh 재시작
  - C에서...
    - RSA key pair 생성하기 : ssh-keygen
	  - passphrase 생성하면 더 좋지만, 없어도 됨 (생성 안할때는 그냥 엔터키 누르면 됨)
    - 생성 후, ~/.ssh 디렉토리 내부에 RSA key pair (id_rsa 파일이랑 id_rsa.pub 파일) 생성 되었는지 확인
    - Key pair 중에서 공개키를 서버에 저장
	  - 서버 IP가 1.2.3.4 이고, 서버에 tom 이라는 계정이 있을 때 : ssh-copy-id tom@1.2.3.4
	- C에서 S로 ssh 접속할 때, 더이상 비밀번호를 물어보지 않음
  - 참고 : https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys-on-ubuntu-1604