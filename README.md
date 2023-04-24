# Jupyter_error_collection
각종 주피터노트북 및 주피터 랩 오류 및 해결 방안


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
