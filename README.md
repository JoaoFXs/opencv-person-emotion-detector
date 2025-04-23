# Facial and Expression Recognition - Image Processing and Computer Vision Exam Project
This project was developed as part of an academic assessment for the Image Processing and Computer Vision course. The system performs facial recognition and emotional expression detection using advanced computer vision techniques.
## Table of Contents

- [Key Features](#key-features)
- [Technologies Used](#technologies-used)
  - [Libraries](#libraries)
- [Installation](#installation)
- [Usage](#usage)
  - [Consume Messages From ActiveMQ](#consume-messages-from-activemq)
  - [Data Transformation and Validation](#data-transformation-and-validation)
  - [Error Handling](#error-handling)
  - [Log Viewing](#log-viewing)
- [Conclusion](#conclusion)
  - [Potential Applications](#potential-applications)
- [Maintainers](#maintainers)
- [Contributing](#contributing)
	- [Contributors](#contributors)
- [License](#license)
  
# Key Features
- Facial Recognition: Identifies faces in images and compares them against a pre-trained database
- Emotion Detection: Classifies facial expressions into 7 categories (angry, disgust, fear, happy, sad, surprise, neutral)
- Training System: Allows training models with new images for personalized recognition
- Result Visualization: Displays images with detected faces and identified emotions

# Technologies Used
- Python 3
## Libraries:
- face_recognition
- dlib
- OpenCV
- scikit-learn
- DeepFace
- Pillow
- seaborn and matplotlib for visualization

# Installation
To run this project, install the dependencies with:
```bash
pip install face_recognition opencv-python scikit-learn seaborn matplotlib deepface
```
# Project Structure
The main code contains:
- Initial setup: Loading pre-trained facial detection models
##Processing functions:
- face_encodings: Generates facial feature vectors
- _raw_face_locations: Detects faces in images
## Model training:
- Data splitting into training, validation, and test sets
## Data normalization
- Logistic Regression training
- Emotion detection: Uses DeepFace library for emotional analysis
- Visualization: Plotting results and confusion matrices

# How to Use
1. Prepare a directory with training images, organized in subfolders by person
2. Execute the main() function with the image folder path and a location to save the model
3. To test with new images, use the process_new_image() function

## Example:
```python
folder_path = "/path/to/training_images"
model_path = "/path/to/trained_model.h5"
```
1. Train or load model
```python
clf, names, scaler = main(folder_path, model_path)
```
2. Test with new image
```python
new_image_path = "/path/to/new_image.jpg"
process_new_image(new_image_path, model_path)
```
# Results
The system provides:
- Person identification (if recognized)
- Detected emotion (with Portuguese translation)
- Face coordinates in the image
- Facial feature vector
- Evaluation metrics (accuracy, F1-score, confusion matrix)

# Limitations
- Requires images with clearly visible faces
- Performance may vary with lighting conditions and angles
- Unregistered persons are classified as "Unknown"

# Maintainers

[@JoaoFXs](https://github.com/JoaoFXs).

## Contributing

- Feel free to dive in! [Open an issue](https://github.com/JoaoFXs/climasync/issues) or submit PRs.
- Climasync follows the [Contributor Covenant](http://contributor-covenant.org/version/1/3/0/) Code of Conduct.

### Contributors

This project exists thanks to all the people who contribute.

[![Contributors](https://contributors-img.web.app/image?repo=JoaoFXs/climasync)](https://github.com/JoaoFXs/climasync/graphs/contributors)


## License

[MIT](LICENSE) © JoaoFXs

Date: November 2023
