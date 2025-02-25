# HR-VISPR - Human Visual-Privacy Dataset

This repository provides access to the **HR-VISPR** proposed for evaluating human visual privacy protection, presented in the paper [conference name]. 
The dataset is derived from the [Visual Privacy Dataset](https://github.com/tribhuvanesh/vpa) proposed by [Orekondy et al.](https://tribhuvanesh.github.io/vpa/)

## Download the Dataset

Download the dataset at [HR-VISPR ](https://drive.google.com/drive/folders/1rH3m8freZ3fMBq7cJ8AXC_gDcppTAOpi?usp=sharing). The following three files are available:  
- `hr-vispr.zip` the original (non-anonymized) HR-VISPR and the privacy labels (available as .json files)
```
hr-vispr/
├── vispr_refined_c2/
│   ├── train2017/
│   │   ├── 2017_imgid.jpg
│   ├── train2017_labels/
│   │   ├── 2017_imgid.json
│   ├── val2017/
│   │   ├── 2017_imgid.jpg
│   ├── val2017_labels/
│   │   ├── 2017_imgid.json
│   ├── test2017/
│   │   ├── 2017_imgid.jpg
│   ├── test2017_labels/
│   │   ├── 2017_imgid.json
│   ├── 7_class_pkl_labels/
│   │   ├── train/val/test2017_labels.pkl
│   ├── 18_class_pkl_labels_with_safe/
│   │   ├── train/val/test2017_labels.pkl
```

- `hrvispr_anonymized.zip` anonymized dataset with 11 methods (as explained in the paper)  
```
hrvispr_anonymized/
├── Human_2D_Avatars/
│   ├── train2017/
│   │   ├── 2017_imgid.jpg
|   |   |    ...
│   ├── val2017/
│   │   ├── 2017_imgid.jpg
|   |   |    ...
│   ├── test2017/
│   │   ├── 2017_imgid.jpg
|   |   |    ...
├── Human_Blurring/
...
```
- `object_detection_utility_labels.zip` the utility labels for the object detection task
```
object_detection_utility_labels/
├── train_labels/
│   ├── 2017_imgid.txt
|   |   ...
├── val_labels/
│   ├── 2017_imgid.txt
|   |   ...
├── test_labels/
│   ├── 2017_imgid.txt
|   |   ...
```
## Privacy 
The privacy lables are applied to train a multi-label binary classifier on the original (non-anonymized) images. Then, the classifier is applied on the anonymized versions, and the privacy protection is quantified by the drop in cMAP. The following repositorities are helpful for this task:
[TeD-SPAD](https://github.com/UCF-CRCV/TeD-SPAD)&[SPAct](https://github.com/DAVEISHAN/SPAct).  

## Utility 
While the utility is chosen to be object detection on a subset of [COCO](https://paperswithcode.com/dataset/coco) labels, other utility tasks can be applied if the ground truth annotations are obtained. 

## Annotation Tool
The dataset annotations were generated with the tool **[[tkteach](https://github.com/rmones/tkteach)]**

