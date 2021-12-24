# Description:
This usecase is built on top of the deepstream_test3.py.<br>
Built using Deepstream SDK and nvdsanalytics on Jetson Nano.<br>
The application is for counting number of cars on Lane1 and Lane2 on the highway. <br>


### Model Tools and SDKs:<br>
    1. This usecase is built on deepstream 5.1 with deepstream-test3 as reference.
    2. ResNet10 caffemodel was used for car detection.
    3. NvDsAnalytics plugin is used for counting cars on Lane1 and Lane2.


## **Project Structure:**<br>

### highway_entry_exit:
        ----- config_nvdsanalytics.txt
        ----- highway_entry_exit.py
        ----- dstest3_pgie_config.txt
        ----- dsnvanalytics_tracker_config.txt
        ----- tracker_config.yml

        -------- model_files
            -------- cal_trt.bin
            -------- labels.txt
            -------- resnet10.caffemodel
            -------- resnet10prototxt

### File explanation:<br>
    1. config_nvdsanalytics.txt: LOI coordinates are defined in this file.
    2. dstest3_pgie_config.txt: model file path and its properties.
    3. dsnvanalytics_tracker_config.txt: define the path to the tracker to be used for inference.
    4. tracker_config.yml: tracker parameters are defined in this file.
    5. highway_entry_exit.py: main file for inference


### Steps to run the project:<br>
1. For running with downloaded video:
> $ python3 deepstream_retail_mgm.py file://< path to the video file>
    
2. For running with rtsp link:
> $ python3 deepstream_retail_mgm.py rtsp://< rtsp link>