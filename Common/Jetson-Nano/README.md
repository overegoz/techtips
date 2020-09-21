# Jetson Nano

## <Install : pre-trained models and deep learning libraries>
- sudo apt update
- sudo apt install git cmake libpython3-dev python3-numpy
- git clone --recursive https://github.com/dusty-nv/jetson-inference
- cd jetson-inference
- mkdir build
- cd build
- cmake ../
- make
- sudo make install
- sudo ldconfig // to link these libraries with your system
- IT'S ALL SET! LET'S TEST SOME
- cd aarch64/bin
- ./detectnet-console.py images/peds_0.jpg output_0.jpg

## <Visual Code on Ubuntu>
- https://linuxize.com/post/how-to-install-visual-studio-code-on-ubuntu-18-04/

## <VNC 설정하기>
- https://medium.com/@bharathsudharsan023/jetson-nano-remote-vnc-access-d1e71c82492b

## <Tutorials>
- Vision recognition neural network demo : LINK
  - ~/Desktop/jetson-inference/build/aarch64/bin 에서
  - ./imagenet-camera googlenet 입력하면 끝 (처음에는 최적화 과정 때문에 오래 기다려야 하는데, 다음부터는 그럴필요 없다고 함)
- Object detection : https://www.youtube.com/watch?v=bcM5AQSAzUY
- Yolo on Jetson Nano
  - Yolo v3를 돌리는 YouTube 영상이 있긴 한데, 성능(fps)이 너무 낮게 나오는듯
  - Tiny Yolo v2 : https://github.com/tsutof/tiny_yolov2_onnx_cam
  
## <주의>
jetson-inference 예제를 사용하기 위해서는 먼저 $sudo ldconfig 명령을 한번 입력 해 주어야 함.