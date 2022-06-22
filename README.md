# Training Splits of Disjoint Cityscapes

This repository contains the training splits for the Class Disjoint Cityscapes used in: _Continual Learning for Class- and Domain-Incremental Semantic
Segmentation_ and _Improving Replay-Based Continual Semantic Segmentation with Smart Data Selection_.

## Format

The splits for each subset are saved in a json-Files that contain a list of dictionaries with paths to the training images and the corresponding labels. The dictionaries  are structured as follows:

```
{
  "img": <RELATIVE_PATH_TO_IMG>,
  "label": <RELATIVE_PATH_TO_LABEL>,
  "id": <TRAIN_ID>
  "weight": 1
}
```

## Class Mapping

The original class_ids are mapped to new set of train_ids for Disjoint Cityscapes. Please check the adjusted [labels.py](labels.py) which is based on the original [Cityscapes implementation](https://github.com/mcordts/cityscapesScripts/blob/master/cityscapesscripts/helpers/labels.py). A example on how to map Cityscapes class ids to trainIds can be found in the notebook [here](labels.ipynb).
