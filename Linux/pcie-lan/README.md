# PCIE-LAN 카드 추가하기

참고 : https://unixblogger.wordpress.com/2016/08/11/how-to-get-your-realtek-rtl8111rtl8168-working-updated-guide/

추가한 PCIE-LAN 카드 : Realtek, RTL8111/8168/8411

랜카드 장착 후 부팅 하여, lspci 명령 입력 하니까 PCIE-LAN 카드가 정상적으로 탐지됨

그런데, ifconfig 명령 입력시, 추가한 랜카드가 안보임

sudo apt-get dist-upgrade; sudo apt update; sudo apt-get install r8168-dkms 명령을 실행

lsmod | grep r8168 명령으로 확인한 결과 r8168 모듈이 정상적으로 설치 된 것을 확인함

lshw 명령의 출력결과 에서, network 하드웨어 중에서 RTL8111/8168/8411 을 찾아서, logical name을 검색해 보니, 랜카드의 이름이 enp3s0 인 것을 확인함

etc > netplan > *.yaml 파일 : 추가한 인터페이스를 DHCP로 설정

sudo netplan apply

끝.
