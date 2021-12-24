![Alt Text](nv_deepstream_apps/ds_retail_management/model_files/retail.gif)


# Description:

The usecase is built on jetson Nano(4GB dev kit)<br>
The usecase inference was executed and tested on jetson Nano.<br>


### This usecase is for retail store management: <br>
    1. Count number of entry and exit in the store.
    2. Count number of people visiting a specific counter.

### Model Tools and SDKs:<br>
    1. This usecase is built on deepstream 5.1 with deepstream-test1 as reference.
    2. ResNet10 caffemodel was used for people detection.
    3. NvDsAnalytics is used for video analytics, entry and exit lines, ROI boxes were drawn using 
    NvDsAnalytics plugin.

## **Project Structure:**<br>

### Retail Analytics:
        ----- config_nvdsanalytics.txt
        ----- deepstream_retail_mgm.py
        ----- dsnvanalytics_pgie_config.txt
        ----- dsnvanalytics_tracker_config.txt
        ----- tracker_config.yml

        -------- model_files
            -------- cal_trt.bin
            -------- labels.txt
            -------- resnet10.caffemodel
            -------- resnet10prototxt

### File explanation:<br>
    1. config_nvdsanalytics.txt: ROI and LOI coordinates are defined in this file.
    2. dsnvanalytics_pgie_config.txt: model file path and its properties.
    3. dsnvanalytics_tracker_config.txt: define the path to the tracker to be used for inference.
    4. tracker_config.yml: tracker parameters are defined in this file.
    5. deepstream_retail_mgm.py: deepstream file with code logic.


### Steps to run the project:<br>
1. For running with downloaded video:
> $ python3 deepstream_retail_mgm.py file://< path to the video file>
    
2. For running with rtsp link:
> $ python3 deepstream_retail_mgm.py rtsp://< rtsp link>

