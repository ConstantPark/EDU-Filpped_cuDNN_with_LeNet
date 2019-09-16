이 게시물은 모두의 연구소 풀잎스쿨 8기 CUDA 강의에서 사용되었습니다.  
(https://github.com/tbennun/cudnn-training 자료를 참고하여 수정하였습니다.)  
(This git page is based on this git page, https://github.com/tbennun/cudnn-training)

사전에 설치되어야 하는 것들 (Prerequisites)
=============

* C++11을 지원하는 컴파일러가 필요합니다 (Visual Studio, GCC)
* CUDA (6.5 이상) 및 cuDNN (v5 이상)
* MNIST 데이터 셋 (http://yann.lecun.com/exdb/mnist/)
* (optional) gflags: https://github.com/gflags/gflags
* CUDNN_PATH를 bash에 등록해야 합니다.  
별도의 세팅 없이 컴파일하여 사용가능하지만, cuDNN의 설치만 필요합니다.  
가급적 리눅스 환경에서 사용하시는 것을 권합니다.

컴파일 방법 (How to build)
===========

* CMake를 사용하여 컴파일 합니다.

CMake를 사용하여 컴파일 하는 과정은 다음과 같습니다.
```bash
~: $ cd cudnn-training/
~/cudnn-training: $ mkdir build
~/cudnn-training: $ cd build/
~/cudnn-training/build: $ cmake ..
~/cudnn-training/build: $ make
```
```CUDNN_PATH```, ```USE_GFLAGS``` 의 설정이 존재합니다.  
```USE_GFLAGS```는 GFLAG를 사용할때만 필요합니다.

Running
=======

* build 폴더 내부에 MNIST의 데이터를 넣어두었습니다. 그냥 실행하시면 됩니다.  
* 컴파일 후에 생성된 바이너리가 있는 폴더 (build)에 MNIST의 데이터가 필요합니다.
* 이후 자동적으로 실행이 됩니다.
* Volta (GV100) 기준으로 0.76ms, TitanX에서 1.54ms, P100에서 1.14ms가 소요됩니다.
