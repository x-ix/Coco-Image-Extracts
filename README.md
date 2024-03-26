---
license: mit
task_categories:
- text-classification
- text-generation
language:
- en
tags:
- code
pretty_name: '*'
size_categories:
- 0.001M<n<0.0011M
---
# Modified Coco Dataset Files

Hugging Face Link: https://huggingface.co/datasets/iix/coco_image_extract

# Required dependencies 

```
OpenCV (cv2):

pip install opencv-python
```

# img_data.psv

Extract of the coco dataset containing the following labels: ```["airplane", "backpack", "cell phone", "handbag", "suitcase", "knife", "laptop", "car"]```

```
Structured as follows:

| Field           | Description                                                                                         |
| --------------- | --------------------------------------------------------------------------------------------------- |
| file_name       | Name of image file (.png)                                                                           |
| height          | Image height prior to padding                                                                       |
| width           | Image width prior to padding                                                                        |
| annotations     | Array of boundary box array, label pairs. Bbox arrays are of the form [x_min, y_min, width, height] |

1.09k rows
```

# /data (folder)

This directory contains a selection of zero-padded COCO images that correspond to img_data.parquet.


# display_boundary.py

Mini gui for viewing images with their boundary boxes, don't need to pay attention to how it works, just do the following:

Ensure you're in the same working directory as display_boundary.py
```
cd mini_coco_dataset
```

```
python display_boundary.py
```

- It takes an image name as input (x.png), to find image names look in the data folder.

If you have any questions or issues, feel free to keep them to yourself.