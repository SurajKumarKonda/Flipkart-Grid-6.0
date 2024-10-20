# **Defect Detection on Conveyor Belt Using YOLOv5 and Arduino**

## **Overview**
This project is an automated defect detection system that leverages the YOLOv5 object detection model for real-time identification of defective items on a conveyor belt. When a defective item is detected, the system communicates with an Arduino via serial communication to trigger a servo motor, which removes the defective item from the conveyor belt.

## **Features**
* **Real-time defect detection:** Uses YOLOv5 for high-speed object detection.
* **Custom-trained model:** Specific defect types can be detected through a custom-trained YOLOv5 model.
* **OpenCV for video feed processing:** Captures and processes the conveyor belt video in real-time.
* **Arduino-controlled servo motor:** Automatically removes defective items from the belt by triggering the servo motor.
* **PyTorch Integration:** PyTorch is used to load and run the YOLOv5 model for inference.

## **Hardware Requirements**
* **Arduino:** Controls the servo motor to remove defective items.
* **Servo Motor:** Physically pushes defective items off the conveyor belt.
* **Conveyor Belt:** Carries items under the camera for inspection.
* **Webcam:** Captures live video feed of the conveyor belt for defect detection.
* **PC:** Runs the Python script and YOLOv5 model for real-time detection.

## **Software Requirements**
* **Python 3.8+**: Required to run the detection scripts and machine learning model.
* **PyTorch:** Framework for loading and running the YOLOv5 object detection model.
* **OpenCV:** For capturing and processing the video feed, as well as displaying the detection results.
* **YOLOv5:** A deep learning model used for defect detection, trained to identify specific defects.
* **Arduino IDE:** To upload the control code to the Arduino for servo motor manipulation.
* **Serial Communication (pyserial):** For establishing communication between the PC and Arduino to synchronize detection and removal actions.

## **Installation**
1. Clone the repository:
    ```bash
    git clone https://github.com/username/defect-detection-conveyor.git
    ```
2. Navigate to the project directory:
    ```bash
    cd defect-detection-conveyor
    ```
3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
4. Upload the Arduino code to the Arduino board:
    * Connect the Arduino to your PC.
    * Open the Arduino IDE and upload `servo_control.ino` to the Arduino.

## **Usage**
1. Start the conveyor belt system and ensure the webcam is positioned correctly over the belt.
2. Run the YOLOv5 Python script to begin defect detection:
    ```bash
    python detect.py --source 0  # 0 is for webcam input
    ```
3. The system will process the video feed, and if a defect is detected, the Arduino will be instructed to activate the servo motor to remove the defective item from the conveyor belt.
4. Visual feedback will be displayed in real-time, showing detected defects on the video feed.

## **Contributing**
If you wish to contribute to this project, please follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

## **License**
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
