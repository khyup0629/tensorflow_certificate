# 텐서플로우 자격증 시험 환경 설치

## 시험 요구 사항 확인

=> https://www.tensorflow.org/extras/cert/Setting_Up_TF_Developer_Certificate_Exam.pdf

+ 위의 URL으로 들어가서 텐서플로우 자격 시험에 필요한 버전에 맞게 설치한다.
+ 21.07.04. 기준 **Python 3.8.x, Pycharm 2021.x, Tensorflow 2.5.0** 버전을 설치해야한다.

> <h3>Anaconda 설치
 
+ Anaconda는 가상 환경을 의미한다. 가상 환경을 설치할 때 **파이썬 버전을 3.8**로 설치할 것이다.

=> https://www.anaconda.com/products/individual

+ 위의 사이트에서 윈도우/맥에 맞는 아나콘다 설치 파일을 다운로드 받는다.
+ exe 설치 파일을 클릭해서 아나콘다 가상환경을 설치한다.
+ (윈도우 기준) 파일 찾기를 검색해 **anaconda prompt**를 검색한다.

> <h3>텐서플로우와 라이브러리 설치

+ 'tf-cert'라는 이름의 가상 환경을 만들어 줄 것이다. 아래의 명령을 프롬프트에 입력해준다.

  conda create -n tf-cert

+ 만든 가상 환경을 활성화한다.
  
  conda activate tf-cert

+ Tensorflow 2.5.0 을 설치한다.
  
  pip install tensorflow==2.5.0
  
+ tensorflow-datasets를 설치한다.
  
  pip install tensorflow-datasets
  
+ numpy를 설치한다.(텐서플로우를 설치할 때 같이 설치될 것이므로 이미 설치되었다(Requirement already satisfied)는 문구가 뜨면 잘 된 것)
  
  pip install numpy
  
+ Pillow를 설치한다.
  
  pip install Pillow
  
+ urllib3를 설치한다.
  
  pip install urllib3
  
+ tensorflow 2.5.0, tensorflow-datasets, numpy, Pillow, urllib3가 모두 잘 설치가 되었는지 확인해본다.
  
  pip freeze
  
![image](https://user-images.githubusercontent.com/43658658/124373188-1bee3580-dccb-11eb-895c-765113dfe5af.png)

+ 5개 모두 잘 설치되어 있는 것을 확인할 수 있다.
  
> <h3>Pycharm에 Anaconda 가상환경 세팅
  
![image](https://user-images.githubusercontent.com/43658658/124373240-8b642500-dccb-11eb-9491-bb998c03e925.png)

+ 파이참 하단에 빨간 동그라미 부분을 클릭해서 'Add interpreter'를 클릭한다.
  
![image](https://user-images.githubusercontent.com/43658658/124373284-fdd50500-dccb-11eb-909c-91184026a2c1.png)

+ 'conda environment'에서 Existing environment의 동그라미 부분에 자동으로 방금 만들어준 가상 환경 경로가 표시된다.
+ 'Make available to all projects'를 체크한다.

+ 다시 파이참 하단의 Add interpreter를 클릭했던 부분을 다시 클릭해서 'Python 3.8 (tf-cert)'로 인터프리터를 바꿔준다.

+ 임의의 py 파일을 하나 만들어서 아래의 코드를 입력한 후 실행한다.

``` python
import tensorflow as tf

print(tf.__version__)
```

![image](https://user-images.githubusercontent.com/43658658/124373313-4d1b3580-dccc-11eb-9d5d-4773ee8a1175.png)

+ 2.5.0 버전이 출력되면 Tensorflow가 올바르게 적용되었다는 뜻이다.
