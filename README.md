# YOLOV11_New-York and Istanbul Streets
## Object Detection and Training Process with YOLOv11
### Methods and Tools Used
1. Python Libraries and Tools:
   - **Ultralytics YOLO:** Perform object detection with the YOLOv11 model and train the model.
   - **Roboflow:** Management and processing of training dataset.
   - **IPython Display:** Showing visuals during the training process.
2. YOLOv11 Model:
   - **Pretrained Model:** Baseline performance was tested using a previously trained YOLOv11 model.
   - **Transfer Learning:** The model is retrained on a customized dataset.
### Project Steps
1. **Preprocess and Uploading Model:**
   Pretrained YOLOv11 model was tested using yolo11n.pt and initial results were analyzed on a ready-made visualization:
   
   ![Ekran görüntüsü 2024-12-02 160548](https://github.com/user-attachments/assets/4e75e8a2-58ea-4b7c-9748-aa193fa87a68)
2. **Fencing Dataset and Training Model:**
   - A custom dataset was downloaded using Roboflow.
   - The images in the dataset are organized in a suitable format to be used in the training process of the model.
   - The model is trained for 50 epochs on a customized dataset.
3. **Validate Model:**
   Accuracy and other metrics of the post-training model were measured on the validation dataset.
4. ** Forecast and Results:**
    - The normalized confusion matrix visualizes the classification performance of the model:
   
   ![Ekran görüntüsü 2024-12-02 161432](https://github.com/user-attachments/assets/b2a0a96f-44a7-497f-83b1-d948a58ad44b)

### Comparison of the Model for Two Different Street Photos

Transferred images of New York and Istanbul were tested with the same model and different results were obtained. The differences in the model's prediction rates can be attributed to several factors.

| New York Street | Istanbul Street |
|----------------------|----------------------|
| ![Ekran görüntüsü 2024-12-02 160548](https://github.com/user-attachments/assets/d9c55e2a-d924-4318-be88-5d4ddba0cc09) |  ![Ekran görüntüsü 2024-12-02 162740](https://github.com/user-attachments/assets/796dc066-65bf-41ed-a84f-42e7b607426c) |

For the photo taken in Istanbul, the model made better predictions in the person class. There may be many reasons for this. The main factors that we have identified are as follows:
#### Parallax:
Differences in parallax result from the horizontal distance between the camera and the object.
#### Relief Displacement:
More pronounced for tall objects or protrusions in perspective images. 
Easily noticeable on small-scale objects, but reference points are usually sufficient for corrections.
#### Resolution:
Cameras are closer to the object, providing higher resolution.
This enables capturing fine details (e.g., architectural elements or intricate surface textures).
#### Image Noise:
Light conditions are easier to control, minimizing noise.
Issues may arise in low-light environments.
#### Perspective Distortion:
Becomes prominent when objects are close, especially with wide-angle lenses.
#### Color Aberration:
Controlled lighting reduces chromatic aberrations.
