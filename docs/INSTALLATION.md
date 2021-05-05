# Installation

The code was tested on Ubuntu **.**, with [Anaconda](https://www.anaconda.com/download) Python 3.* and [PyTorch]((http://pytorch.org/)) v1.5.* NVIDIA GPUs are needed for both training and testing.
After install Anaconda:

0. [Optional but recommended] create a new conda environment with your project name prjname. 

    ~~~
    conda create --name prjname python=3.*6*
    ~~~
    And activate the environment.
    
    ~~~
    conda activate prjname
    ~~~

1. Install pytorch1.5.*:

    ~~~
    conda install pytorch=0.4.1 torchvision -c pytorch
    ~~~
    
     
2. Install other dependencies (e.g. [COCOAPI](https://github.com/cocodataset/cocoapi)):

    ~~~
    # COCOAPI=/path/to/clone/cocoapi
    git clone https://github.com/cocodataset/cocoapi.git $COCOAPI
    cd $COCOAPI/PythonAPI
    make
    python setup.py install --user
    ~~~

3. Clone this repo:

    ~~~
    prjname_ROOT=/path/to/clone/prjname
    git clone https://github.com/xingyizhou/prjname $prjname_ROOT
    ~~~


4. Install the requirements

    ~~~
    pip install -r requirements.txt
    ~~~
    
    
5. Compilation.

    ~~~
    cd $prjname_ROOT//lib/networks/***
    ./make.sh
    ~~~

7. Download pertained models and move them to `$prjname_ROOT/models/`. More models can be found in [Model zoo](MODEL_ZOO.md).
