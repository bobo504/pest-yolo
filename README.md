# pest-yolo
Pest-yolo: A lightweight YOLOv5n-based pest detection algorithm
# usage
The MobileNetv3, LCnet, and Ghostnet are defined in models/common.py.
These modules are registered in yolo.py.
The lightweight backbones are configured in models/yolo5n_pest/*.py.
CBAM is defined in cbam.py
# Environment Configuration
Please see requirements.txt
It is strongly recommended to use the latest YOLOv5 repository and integrate the above files into the latest code.
YOLOv5:https://github.com/ultralytics/yolov5
# Trained Weight File for detecting 8 pests
8 pests: rice leaf roller, grub, wireworm, aphids, blister beetle, Miridae, unaspis_yanonensis, and Cicadellidae.
The trained weight file is available at: https://drive.google.com/drive/folders/1lNFcXtO-4-Wrbmzxuebt8lxpbqON1DTU?usp=drive_link
pest-yolo-ip102.pt is the weight file for 102 pests.
# Performance comparison of integrating CBAM

Model	      Precision	    Recall	    mAP50	          mAP50-95	 Parameters

YOLOv5n	    0.895	        0.91      	0.927	          0.525	     1,769,989

YOLOv5n-M3	0.861	        0.87	      0.895 (-3.2%)	  0.476	     1,171,493 (-33.8%)

Pest-YOLO	  0.864	        0.874	      0.903 (-2.4%)	  0.478	     1,185,972 (-33%)

# Performance comparison of different lightweight backbones
Model	            Precision	    Recall	    mAP50	          mAP50-95	 Parameters

YOLOv5n-ghostnet	0.843         0.844       0.892           0.473	     1,362,697

YOLOv5n-lcnet	    0.866         0.843       0.894           0.495	     1,188,349

Pest-YOLO	        0.864	        0.874	      0.903	          0.478	     1,185,972

# The pest-yolo-ip102 model performance
Model	            Precision	    Recall	    mAP50	          mAP50-95

pest-yolo-ip102   0.547         0.583       0.559           0.333

