## YOLOv26 Real Time Instance Segmentation Android Application

### Description
This Android application is designed to perform Instance Segmentation using the YOLOv26 machine learning model. This app brings instance segmentation functionality to Android devices by using camera frames in real time.

### YOLOv26 output format
This sample supports YOLOv26 end-to-end instance segmentation TFLite exports with outputs like:

- Detection output: `[1, 300, 38]`
- Mask prototype output: `[1, 160, 160, 32]`

The detection output is parsed as `[x1, y1, x2, y2, confidence, class_id, mask_coefficients...]`.
The YOLOv26 parser does not run Android-side NMS because the export is already end-to-end.
Class labels are loaded from Ultralytics metadata embedded in the `.tflite` model.

### Getting Started
To use this repository for a custom YOLOv26 instance segmentation model, follow these steps:
1. Clone this repository to your local machine.
2. Put your exported `.tflite` model inside the `app/src/main/assets` folder.
3. Update the `modelPath` value in `MainActivity.kt` if your model file name is different.
4. Build and run the Android app.

### Contributing
Contributions are welcome! If you want to contribute to this project, feel free to fork the repository and submit a pull request with your changes.

### Contact
For any questions or feedback, feel free to open an [issue](https://github.com/surendramaran/YOLO/issues/new) in the repository.

### Support
If you find this project helpful and want to support its development, consider becoming a patron on [Patreon](https://www.patreon.com/SurendraMaran). Your support will help in maintaining and improving the project. Thank you!
