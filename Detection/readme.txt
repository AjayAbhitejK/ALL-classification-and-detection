This folder contains the training and testing scripts of the YOLO models for detection of ALL:
The dataset used is from 'Roboflow' which contains 1500 annotated images from C-NMC dataset.
Models tested are:
- YOLOv5n
- YOLOv8n
- YOLO11n

Note that these models are taken from the Ultralytics package and the smallest 
versions(i.e. with suffix 'n') of the respective YOLO models were used due 
to time and resource constraints. Additionally, two image sizes were tested 
i.e., 224x224 and 640x640 to observe any performance difference.

Here are the performance metrics values of each model after 250 epochs:
| Model-image size | Precision |	Recall	| mAP@.5	| mAP@.5-.95 |	Parameters |
| :--------------: | :-------: |  :-------:  | :-------:  | :--------: | :---------: |
|     YOLOv5n – 224    |    90.0	 |   89.7	 |  91.2	|  76.3	 |  17,61,871 |
|     YOLOv8n – 224    |    83.4	 |   92.7	 |  95.8	|  79.1	 |  30,06,038 |
|     YOLO11n – 224    |    85.3	 |   94.4	 |  96.3	|  79.7	 |  25,82,542 |
|     YOLOv5n – 640    |    90.2	 |   88.4	 |  91.1	|  76.8	 |  17,61,871 |
|     YOLOv8n – 640    |    90.4	 |   89.8	 |  95.9	|  79.8	 |  30,06,038 |
|     YOLO11n – 640    |    89.7	 |   91.2	 |  95.7	|  79.5	 |  25,82,542 |

If you choose to run inference on test sets using YOLOv8n and YOLO11n models, 
the 'val' path(/content/datasets/Acute-Lymphoblastic-Leukemia-3/valid) must be
changed to point to the test path in the configuration files(data.yaml) of the 
respective models explicitly.

