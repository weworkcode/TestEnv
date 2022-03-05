# TestEnv
Testing Env

T81-558: Applications of Deep Neural Networks
Manual Python Setup

Instructor: Jeff Heaton, McKelvey School of Engineering, Washington University in St. Louis
For more information visit the class website.
Software Installation (Mac)
This class is technically oriented. A successful student needs to be able to compile and execute Python code that makes use of TensorFlow for deep learning. There are two options for you to accomplish this:

Install Python, TensorFlow and some IDE (Jupyter, TensorFlow, and others)
Use Google CoLab in the cloud
Installing Python and TensorFlow
Deep Learning on a Mac is in a bit of a state of flux. Mac has not supported NVIDIA GPUs since 2016. With this change, Mac was no longer a serious option for deep learning. Additionally, as of Jun 25, 2017, TensorFlow version 1.2, support for GPU on the Mac version of TensorFlow was dropped. However, all is not entirely lost on the Mac platform. With the introduction of the M1 chip, Apple introduced essentially a system on a chip. The new Mac M1 contains CPU, GPU, and deep learning hardware support. Apple is making available a M1 build of TensorFlow. This build is very new technology and will take some work to make run correctly at this point. As of January, 2021, I have not yet worked with Apple M1. If you are interested in trying this technology, you can read more here. You must have one of the 2020, Mac M1 models to use this release.

Accelerating TensorFlow Performance on Mac
The following instructions install TensorFlow onto a Mac with no hardware acceleration (GPU).

The first step is to install the latest version of Python 3.x. As of January, 2021, this is the latest version of Python 3.8 (install 3.9 or later, if it is available). I recommend using the Miniconda (Anaconda) release of Python, as it already includes many of the data science related packages that are needed by this class. Anaconda directly supports Windows, Mac, and Linux. Miniconda is the minimal set of features from the extensive Anaconda Python distribution. Download Miniconda from the following URL:

Miniconda
First, lets install Jupyter, which is the editor you will use in this course.

conda install -y jupyter
We will actually launch Jupyter later.

Next we will install the Mac tensorflow.yml file that I provide. Run the following command from the same directory that contains tensorflow.yml.

conda env create -f tensorflow.yml -n tensorflow
To enter this environment, you must use the following command:

conda activate tensorflow
For now, lets add Jupyter support to your new environment.

conda install nb_conda
Register your Environment
The following command registers your tensorflow environment. Again, make sure you "conda activate" your new tensorflow environment.

python -m ipykernel install --user --name tensorflow --display-name "Python 3.8 (tensorflow)"
