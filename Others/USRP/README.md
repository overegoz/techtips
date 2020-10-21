# USRP

## 설치 : 리눅스, Ubuntu
- https://kb.ettus.com/N200/N210_Getting_Started_Guides#Install_and_Setup_the_Software_Tools_on_Your_Host_Computer
- https://kb.ettus.com/Building_and_Installing_the_USRP_Open-Source_Toolchain_(UHD_and_GNU_Radio)_on_Linux
- HOST PC 의 IP 설정
  - 192.168.10.1 / 24
  - GW: 0.0.0.0, DNS: 0.0.0.0
- 설치 후,
  - uhd_find_devices
  - uhd_usrp_probe
  - 입력해서 연결 되는지 확인
  - F/W 또는 FPGA 업데이트 하라고 나오면...
  - Firmware/FPGA 업데이트
    - /usr/local/lib/uhd/utils/uhd_images_downloader.py
    - /usr/local/bin/uhd_image_loader --args="type=usrp2,addr=192.168.10.2"
    - 이렇게만 입력하면 자동으로 업로드 됨
    - 그리고 USRP 장비를 재부팅 해야지 적용이 됨
  - 192.168.10.2로 ping 이 안보내지면, (USRP는 기본적으로 192.168.10.2 IP를 사용)
    - $route 명령으로, 라우팅 경로 있는지 확인하고, 없다면
    - $route add -net 192.168.10.0 netmask  255.255.255.0 dev <Eth 카드 이름>

## 설치 : 윈도우, Win-10
- https://kb.ettus.com/N200/N210_Getting_Started_Guides#Install_and_Setup_the_Software_Tools_on_Your_Host_Computer
- https://kb.ettus.com/Building_and_Installing_the_USRP_Open_Source_Toolchain_(UHD_and_GNU_Radio)_on_Windows
