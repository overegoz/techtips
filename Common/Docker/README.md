# docker image
https://www.tensorflow.org/install/docker
docker pull tensorflow/tensorflow:1.15.0-gpu-py3-jupyter
 
# docker run
docker run \

--gpus all \  ** 모든 GPU 사용하도록 지정

-it \  ** interactive over terminal

-p 8888:8888 \  ** 포트매핑 또는 포워딩

-v /alsolute/path/to/shared/dir:/target/dir \  ** 디렉토리 공유

tensorflow/tensorflow:1.15.0-gpu-py3-jupyter  ** 실행할 이미지 지정

TIP
  - tip<-p>!! port mapping is [로컬 컴퓨터 포트]:8888
  - tip<-v 절대경로>!! target dir은 존재하지 않는 경로여도 괜찮 (보통은 /tf/shared 정도로 쓰면 될 듯. Jupyter가 /tf 아래에서 시작하니까?)
  - OpenCV Docker error "ImportError: libSM.so.6: cannot open shared object file: No such file or directory" 와 같은 오류가 발생하면...
    - apt-get update
    - apt-get install -y libsm6 libxext6 libxrender-dev
    - pip install opencv-python