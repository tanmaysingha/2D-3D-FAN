# Pytorch version of 'How far are we from solving the 2D & 3D Face Alignment problem?
Please refer to face-alignment-training [https://github.com/1adrianb/face-alignment-training] for official torch7 version.
This work is a reinplemention of training code for 2D-FAN and 3D-FAN decribed in "How far" paper. Please visit author's webpage [https://www.adrianbulat.com] or arxiv [https://arxiv.org/abs/1703.07332] for technical details.
There are few Pytorch versions of 2D/3D FAN model in GitHub, but most of the reimplementations have issues in the training scripts. This GitHub repository resolved those issues and trained the model with the most challenging 2D/3D LS3D-W datasets. It also provides the weights of FAN model for landmarks localization and S3FD model for face detection. This repository adobts some codes from other GitHub repositories for reference, such as pyhowfar, face-alignment, face-alignment-pytorch. 

# Requirements
 Install the latest Pytorch [http://pytorch.org].
 
 # Packages
 scipy==1.1.0
 torchvision==0.7.0
 progress
 CUDA
 CUDNN
 matplotlib
 opencv-python
 scikit-image
 
 # Weights of FAN and S3FD models
 Download weight of 3D-FAN model from the following link: 
 https://drive.google.com/file/d/1NmXw-gaAibY4HaoEMY3MQD7E2VvyLHtD/view?usp=sharing
 
 Download weight of S3FD model from the following link:
 https://drive.google.com/file/d/1RPqjxmli69V9vpez3gRFo-6jdTppX5gm/view?usp=sharing
 
 # Setup for inference
 1. Clone the repository:
 git clone https://github.com/tanmaysingha/2D-3D-FAN
 
 2. Installl all the dependencies mentioned above:
 pip install -r requirements.txt
 
 3. Download weights from the above mentioned links.
 
 4. Chnage the working directory:
 cd 2D-3D-FAN
 
 5. Run the python script inference.py:
 python inference.py --modelfile "path of the weight of 3D-FAN model" --detectmodelfile "Path of the weight of S3FD model" --input "path of the input image"
 
 # Setup for training
  1. Clone the repository:
 git clone https://github.com/tanmaysingha/2D-3D-FAN
 
 2. Installl all the dependencies mentioned above:
 pip install -r requirements.txt
 
 3. Download the LS3D-W dataset from the authors webpage (https://www.adrianbulat.com/face-alignment).
 
 4. Download the 300W-LP annotations converted to t7 format by paper author from (https://www.adrianbulat.com/downloads/FaceAlignment/landmarks.zip).
 
 5. Create a "Data" directory under the main project directory (2d-3D-FAN). If you want to train the model with large LS3D-W datasets, then Keep all the datasets and annotations under the "Data" directory.
 
 # Facial landmarks prediction by 2D- FAN
 https://github.com/tanmaysingha/2D-3D-FAN/blob/main/2D-results/2D-landmarks.jpg; 
 
 # Citation
 
 {
   @inproceedings{bulat2017far,
     title={How far are we from solving the 2D \& 3D Face Alignment problem? (and a dataset of 230,000 3D facial landmarks)},
     author={Bulat, Adrian and Tzimiropoulos, Georgios},
     booktitle={International Conference on Computer Vision},
     year={2017}
   }
 
