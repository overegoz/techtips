# RPi 사용 법...


## LCD Rotate (화면 뒤집기)
In Terminal: sudo nano /boot/config.txt
Add line: lcd_rotate=2


## Touch screen calibration (터치 스크린 입력)
- 방법 1
  - sudo apt-get install xinput-calibrator
  - Then, go to [Menu > Preferences > Calibrate Touchscreen]
- 방법 2
  - sudo apt-get install libsdl2-dev libsdl2-ttf-dev
  - cd /tmp
  - wget https://github.com/gamelaster/evdev-calibration/releases/download/0.2/evdev-calibration-armv7.tar.gz
  - tar xvf evdev-calibration-armv7.tar.gz
  - export DISPLAY=:0
  - ./evdev-calibration
  - [주의] There is no support for rotated displays
  
## 가상 키보드
  - sudo apt install matchbox-keyboard
  - src: https://pimylifeup.com/raspberry-pi-on-screen-keyboard/
  - 실행방법
    - Menu > Accessories > Keyboard
    - 터미널에서 실행 : matchbox-keyboard
    - ssh 로 실행 : DISPLAY=:0 matchbox-keyboard &
