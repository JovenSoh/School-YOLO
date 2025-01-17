<p align="center"><img src ='display/logo.png' alt= 'HCIRS LOGO' height = 300 width = 600></p>


<p align="center">>>Made by <a href = https://github.com/JovenSoh>Joven Soh</a>, <a href = https://github.com/DESU-CLUB>DESU-CLUB</a>, <a href = https://github.com/MartinZhouuuuu>MartinZhouuuuu</a> and <a href = https://github.com/Waldeinsamkeit-917>Waldeinsamkeit-917</a></p>

# School-YOLO
A project to assist Hwa Chong in automating their Covid-19 monitoring operations in the canteen

# Disambiguation
 The code written here is to check the social distancing of students and to detect the number of students in the canteen.  
 
 To find the code where the students are tracked by the DEEPSORT algorithm, please head over to the branch found [here](https://github.com/DESU-CLUB/School-YOLO/tree/deepsort-tracker)


# Quick Start
 1) Download YOLOv3 weights from [here](https://drive.google.com/file/d/1uvXFacPnrSMw6ldWTyLLjGLETlEsUvcE/view) (yolo.h5 model file with tf-1.4.0) , put it into model_data folder.  
 2) cd to School YOLO folder  
 3) Run the code with cmd (Recommended if your computer has a powerful GPU): 
 ```
     pip install -r requirements.txt
     python3 Combined_GUI.py
 ```
 After a while, the video files should be outputted in output_videos folder 
 
 You can view the files named detections.mov and minimap.mov
 
 # Quick Start: (But its Colab for those without GPUs)
  ## Using [Google Colab](https://colab.research.google.com/drive/1ajZg1GMya7cyMzncmQe0aks0Gcc9xuMy?usp=sharing): 
 1) Remember to make a copy of the file before starting    
    To do so, go to 'File' (Right under name of the Colab file)   
    Click on 'Save a copy in Drive'
 2) Put a sample video in /input_videos  
 3) Run it with the instructions given

# User Input required  
1) Video Path Flag
```
Input video path here:
```
Just input the path of the video <strong>to be processed</strong> here

2) Calibration Flag
```
Do you wish to calibrate the input?(Y/N):
```
This flag is to check whether user would like to modify the Bird Eyes View Transformation of the image

3) Social-Distancing Flag
```
Do you want to check the social distance (Y/N):
```
This flag is to check whether user would like to include a visual representation of whether students are socially distanced


# Output 
## If Social-Distancing Flag is set to true (You answered yes to the 3rd qn asked)
2 files, named detections.mov and minimap.mov

![detections](display/detections.gif)

![minimap](display/minimap.gif)  
## If Social Distancing Flag is set to False (You answered no to the 3rd qn asked)
![best-output](display/bestoutput.gif)

# Dependencies 
This code can only be run on Python 3.7, with the following dependencies:
```
tensorflow==1.13.2 
numpy==1.18.1
opencv_python==4.1.2.30
Keras==2.3.1
scipy==1.4.1
matplotlib==3.1.2
Pillow==7.2.0
scikit_learn==0.23.1

```

# Acknowledgements
Some baseline code was pulled from QiDian's respository found [here](https://github.com/Qidian213/deep_sort_yolov3) <br>

This project was made by: <br>
[Soh Wei Kiat](https://github.com/JovenSoh)<br>
[Warren Low](https://github.com/DESU-CLUB)<br>
[Zhou Chengyang](https://github.com/MartinZhouuuuu)<br>
[Xue Yuqing](https://github.com/Waldeinsamkeit-917)<br>

# License
## MIT LICENSE
Copyright 2020 HCIRS ML Division

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

    
    
