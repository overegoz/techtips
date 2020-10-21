# OrangePi

## <SD Card : resize 하기>
- sudo armbian-config 에서 System 에서 Firmware 한 후, 모두 다 업그레이드
- 다음으로, sudo resize2fs /dev/mmcblk0p1 하면 끝.

## <패키지 관리>
- sudo apt install python-h5py python3-h5py -y
- sudo apt install tensorflow==1.14.0 (OrangePi 에서 1.14.0 으로 업그레이드는 실패
- sudo pip3 install keras==2.1.5 (최신 버전은 오류가 나는 듯)

## <공식 이미지 설치>
- https://www.armbian.com/orange-pi-lite/ 에 가면, 공식 이미지 다운받을 수 있음
- Bionic 버전이 Ubuntu 기반이라고 함
- 공식 이미지 기본 계정은 root/1234 이고, 최초 로그인 시 root 계정의 비번을 바꾸도록 안내하고, 즉시 사용자 계정을 추가하도록 안내함. 추가된 사용자 계정은 sudo 권한이 부여됨
- sudo armbian-config > system > firware 업데이트 한번 하자
- 기본 이미지는 부팅 후 터미널로 로그인 함. X-window 설치 안되 있는 것 같음.
  - sudo armbian-config > system > desktop 설치하면 desktop 설치되는 듯???
- vnc server 설치
  - https://diyprojects.io/armbian-access-remote-desktop-orange-pi-vnc/#.Xp-qeMgzYuU
  - sudo apt-get install tightvncserver
  - vnc 서버 시작 : vncserver :1 (포트 1번에서 시작)
    - 이때, vnc 접속을 위한 비번을 물어봄
  - vnc 동작 확인 ps -ef | grep Xtightvnc
  - vnc 중지 하려면 vncserver -kill :1
  - 클라이언트에서 접속 하려면 IP::5901 로 접속