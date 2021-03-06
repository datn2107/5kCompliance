# 5kCompilance

This is the source code of AI Challenge Contest 2021.

# Solution Description

* First we are using YoloV5 (threshold 0.25) to draw the green box for mask face and the red box for non-mask face
  ![](https://github.com/datn2107/5kCompilance/blob/master/example.png)
* Then feeding those image into model DenseNet161 to classify mask
* And feeding those image into 2 models DenseNet161 and RegNet_y_8gf to classify distancing (ensemble by take average of
  two output)

# Install
```shell
$ pip install -r requirements.txt 
```

# Download Checkpoint 
All checkpoint available in this [link](https://drive.google.com/file/d/16W69z1dSle_hT_JE4PA8TtHcvuBJ3JEp/view).
Download, extract and put them into saved_models folder. 


# Predict tutorial

``` shell
$ predict.sh
```
It will automatically get data from `../data` which has one `../data/images` directory contains all images and one
../data/*.csv metadata file which has labels of all iamges The result will export to `../result/submission.csv`
