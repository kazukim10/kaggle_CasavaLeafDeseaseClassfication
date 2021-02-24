# Casava_Leaf_DeseaseClassfication
https://www.kaggle.com/c/cassava-leaf-disease-classification

- LeaderBoard 30th /3,900teams
- Private Score 0.9010
- Public Score 0.9018

## Summary
My final submission is ensemble of EfficientNetB5 with Noisy Student 
and ResNext50(32x4d).

## Datasets
This competition datasets only.
(I don't use 2019 datasets.)

## Preprocessing
Image size 512
Augumentations
- ResizeCrop
- Horizontal,VerticalFlip
- OneOf(RandomBrightness, RandomContrast)
- OneOf (RandomBlur,MedianBlur,GaussianBlur)
- ShiftScaleRotate
- Normalize

## Training
- Optimizer Adam
- Loss fuction CrossEntropyLoss

## Base Model CV
CV is StratifiedKFold 5 folds.

- EfficientNetB5
-- CV average 0.8898
-- Public 0.894
-- Private 0.897

- ResNext50(32x4d)
-- CV average 0.8898
-- Public 0.896
-- Private 0.894
