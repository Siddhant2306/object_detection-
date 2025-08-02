# object_detection-

# Space Station Object Detection using YOLOv8

## Training Details

We trained our model for 5 epochs using synthetic images from Falcon. The model learns to detect 3 things inside a space station — fire extinguisher, toolbox, and oxygen tank.

### Epoch-wise Progress

| Epoch | GPU Used | Box Loss | Class Loss | DFL Loss | Examples | Image Size | Precision | Recall | mAP50 | mAP50-95 |
|-------|----------|----------|------------|----------|----------|-------------|-----------|--------|-------|-----------|
| 1     | 3.72 GB  | 1.072    | 3.264      | 1.248    | 19       | 640         | 0.438     | 0.405  | 0.276 | 0.177     |
| 2     | 3.48 GB  | 1.199    | 2.368      | 1.226    | 23       | 640         | 0.484     | 0.385  | 0.368 | 0.208     |
| 3     | 3.77 GB  | 1.122    | 2.316      | 1.169    | 21       | 640         | 0.801     | 0.598  | 0.707 | 0.536     |
| 4     | 3.51 GB  | 0.903    | 1.221      | 1.041    | 16       | 640         | 0.936     | 0.766  | 0.850 | 0.655     |
| 5     | 3.51 GB  | 0.662    | 0.748      | 0.942    | 25       | 640         | 0.974     | 0.840  | 0.905 | 0.793     |

### Final Training Accuracy (for each object)

| Object           | Images | Total Boxes | Precision | Recall | mAP50 | mAP50-95 |
|------------------|--------|-------------|-----------|--------|-------|-----------|
| All Classes      | 154    | 206         | 0.974     | 0.840  | 0.904 | 0.793     |
| Fire Extinguisher| 67     | 67          | 0.977     | 0.925  | 0.946 | 0.816     |
| ToolBox          | 60     | 60          | 0.977     | 0.850  | 0.910 | 0.854     |
| Oxygen Tank      | 79     | 79          | 0.967     | 0.746  | 0.858 | 0.710     |

### Final Predictions on Test Data

| Object           | Images | Total Boxes | Precision | Recall | mAP50 | mAP50-95 |
|------------------|--------|-------------|-----------|--------|-------|-----------|
| All Classes      | 400    | 560         | 0.895     | 0.722  | 0.806 | 0.679     |
| Fire Extinguisher| 183    | 183         | 0.881     | 0.776  | 0.839 | 0.689     |
| ToolBox          | 193    | 193         | 0.904     | 0.710  | 0.806 | 0.723     |
| Oxygen Tank      | 184    | 184         | 0.901     | 0.679  | 0.774 | 0.626     |

---

## How to Run It

1. Install Anaconda (if not already)
2. Download this project folder
3. Open Anaconda Prompt and go to this folder
4. Run:
   ```bash
   setup_env.bat
