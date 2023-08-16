
# Face Blurring Tool

This tool allows users to automatically detect faces in an image and apply a blurring effect to the detected faces.

## Features:
- Uses pre-trained DNN model from OpenCV for face detection.
- Provides an option to choose which face(s) to keep in focus (not blurred).
- Offers adjustable blurring intensity.

## Requirements:
- numpy
- matplotlib
- OpenCV (cv2)
  
## Installation:
1. Clone the repository to your local machine:
```
git clone [URL of the GitHub repo]
```

2. Navigate to the cloned directory and install the required packages:
```
pip install numpy matplotlib opencv-python
```

## Usage:
1. Ensure the model files (`res10_300x300_ssd_iter_140000.caffemodel` and `deploy.prototxt`) are in the correct directory.
2. Load your image.
3. Run the `face_blur_rect` function with the loaded image.

Example:
```python
img1 = cv2.imread('path_to_your_image.jpg', cv2.IMREAD_COLOR)
img1_rect = face_blur_rect(img1, net, factor=2)
```

4. The program will display the detected faces with unique IDs. Enter the unique ID of the face you don't want to blur.
5. The resulting image will have all other faces blurred.

## Contribution:
If you want to contribute to this project, please fork the repository and submit a pull request.

## License:
This project is licensed under the MIT License - see the `LICENSE.md` file for details.
