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

* CMAKE를 사용하여 컴파일 합니다.

To compile with CMake, run the following commands:
```bash
~: $ cd cudnn-training/
~/cudnn-training: $ mkdir build
~/cudnn-training: $ cd build/
~/cudnn-training/build: $ cmake ..
~/cudnn-training/build: $ make
```

If compiling under linux, make sure to either set the ```CUDNN_PATH``` environment variable to the path CUDNN is installed to, or extract CUDNN to the CUDA toolkit path.

To enable gflags support, uncomment the line in CMakeLists.txt. In the Visual Studio project, define the macro ```USE_GFLAGS```.

Running
=======

Extract the MNIST training and test set files (*-ubyte) to a directory (if gflags are not used, the default is the current path).

You can also load and save pre-trained weights (e.g., published along with CUDNN), using the "pretrained" and "save_data" flags respectively.

(build 폴더 내부에 MNIST의 데이터를 넣어두었습니다. 그냥 실행하시면 됩니다)


Running
=======
