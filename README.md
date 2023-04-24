# Jupyter_error_collection
각종 주피터노트북 및 주피터 랩 관련 오류 및 해결 방안


<h1> 1.주피터 랩 서버 다운 </h1>

### 증상
주피터랩 실행 하고 5초 이내 서버 끊김

### 오류코드
**[IPKernelApp] WARNING | Parent appears to have exited, shutting down.**

### 해결책
1.c드라이브-> 사용자 -> '사용자아이디' -> 주피터기본폴더 -> .ipynb_checkpoints 폴더 안의 파일 삭제

### Follw-up
여러번 반복시, 자동으로 .ipynb_checkpoints 폴더 안의 파일이 생성되며 서버가 끊기는데 서버 끊기기전 파일을 빠른속도로 삭제하면 괜찮아짐
영구해결책: 작업 디렉토리를 다른곳으로 변경하고, .ipynb_checkpoints 폴더 외의 다른 사용하던 파일을 옮긴다.

<h1> 2.딥러닝 시 GPU 사용 불가 </h1>

### 증상
import tensorflow as tf
from tensorflow.python.client import device_lib
device_lib.list_local_devices()

같은걸로 확인하였을때 cpu 밖에 안잡힘.

### 오류코드
tf.config.list_physical_devices('GPU') => []
print(torch.cuda.is_available()) => False

### 해결책
1. 윈도우에서는 GPU를 tensorflow==2.10 까지만 지원하므로 이버전을 설치하셈
2. https://discuss.pytorch.kr/t/cuda/1277

### Follw-up
ㅇ\
