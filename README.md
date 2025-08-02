# object_detection-

## Training Details

### Epoch-wise Results

| Epoch | GPU Memory | Box Loss | Cls Loss | DFL Loss | Instances | Size | Precision | Recall | mAP50 | mAP50-95 |
|-------|------------|----------|----------|----------|-----------|------|-----------|--------|-------|----------|
| 1     | 3.72G      | 1.072    | 3.264    | 1.248    | 19        | 640  | 0.438     | 0.405  | 0.276 | 0.177    |
| 2     | 3.48G      | 1.199    | 2.368    | 1.226    | 23        | 640  | 0.484     | 0.385  | 0.368 | 0.208    |
| 3     | 3.77G      | 1.122    | 2.316    | 1.169    | 21        | 640  | 0.801     | 0.598  | 0.707 | 0.536    |
| 4     | 3.51G      | 0.9038   | 1.221    | 1.041    | 16        | 640  | 0.936     | 0.766  | 0.850 | 0.655    |
| 5     | 3.51G      | 0.6619   | 0.7486   | 0.9421   | 25        | 640  | 0.974     | 0.840  | 0.905 | 0.793    |

---

###  Final Class-wise Training Performance

| Class            | Images | Instances | Precision | Recall | mAP50 | mAP50-95 |
|------------------|--------|-----------|-----------|--------|-------|----------|
| *All Classes*  | 154    | 206       | 0.974     | 0.840  | 0.904 | 0.793    |
| FireExtinguisher | 67     | 67        | 0.977     | 0.925  | 0.946 | 0.816    |
| ToolBox          | 60     | 60        | 0.977     | 0.850  | 0.910 | 0.854    |
| OxygenTank       | 79     | 79        | 0.967     | 0.746  | 0.858 | 0.710    |

---

### Final Class-wise Prediction Results

| Class            | Images | Instances | Precision | Recall | mAP50 | mAP50-95 |
|------------------|--------|-----------|-----------|--------|-------|----------|
| *All Classes*  | 400    | 560       | 0.895     | 0.722  | 0.806 | 0.679    |
| FireExtinguisher | 183    | 183       | 0.881     | 0.776  | 0.839 | 0.689    |
| ToolBox          | 193    | 193       | 0.904     | 0.710  | 0.806 | 0.723    |
| OxygenTank       | 184    | 184       | 0.901     | 0.679  | 0.774 | 0.626    |

---

##  Summary

- We used *YOLOv8* to train a model on synthetic space station images provided by *Falcon*.
- The training was done using the scripts from the dataset, with no custom model code.
- Object detection was performed on *FireExtinguisher, **ToolBox, and **OxygenTank*.
- Performance improved with each epoch, reaching up to *0.905 mAP50* in training and *0.806 mAP50* on prediction data.
- The model showed stable results across all classes in both training and testing phases.

---

## Conclusion

We used the provided dataset and training scripts to run a YOLOv8 model that detects important safety objects in synthetic space station images. We did not write the full code, but followed the steps using Anaconda, PyTorch, and Ultralytics libraries.

The model showed strong improvement with each epoch and reached a good level of accuracy by the end. This proves that AI models can be trained effectively on synthetic data and still perform well. This method is useful for space applications and other places where real data is hard to collect.

---

## Technologies Used

- Anaconda for environment management  
- PyTorch as the deep learning framework  
- CUDA for GPU acceleration  
- Ultralytics for YOLOv8 training and prediction  
- OpenCV for image processing and display  
- YOLOv8 for object detection


