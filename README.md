# OpenCV Image Processing and CNN

A complete hands-on Computer Vision project built with Python, OpenCV, NumPy, Matplotlib, Scikit-learn, and TensorFlow/Keras.

I developed this project as a Google Colab-ready OpenCV learning and demonstration notebook. It progresses from fundamental image processing to advanced computer vision, face detection and recognition, and finally a CNN-based Simpsons character classification capstone.

## Project Overview

| Section | Area | Main Topics |
|---|---|---|
| 1 | OpenCV Basics | Image reading, grayscale, resizing, drawing, transformations, thresholding, contours, video |
| 2 | Advanced OpenCV | Color spaces, channels, blurring, bitwise operations, masking, histograms, gradients, edge detection |
| 3 | Face Detection & Recognition | Haar Cascade detection, LBPH recognition, training, saving and loading models |
| 4 | Simpsons CNN Capstone | Dataset preparation, preprocessing, CNN training, evaluation, confusion matrix, classification report and prediction |

## Objectives

In this project, I:
- Learn and demonstrate fundamental OpenCV operations.
- Work with images and video.
- Resize, crop, transform and annotate images.
- Use grayscale conversion, thresholding, contours and edge detection.
- Work with BGR, RGB, HSV and other image representations.
- Use filtering, masking, histograms and bitwise operations.
- Detect faces using Haar Cascade classifiers.
- Train and use an LBPH face-recognition model.
- Build a complete image-classification pipeline with TensorFlow/Keras.
- Train a CNN to classify Simpsons characters.
- Evaluate the CNN using accuracy, loss, confusion matrix and classification metrics.
- Test the model on individual and uploaded images.

## Technologies

- Python 3
- OpenCV / OpenCV Contrib
- NumPy
- Matplotlib
- Scikit-learn
- TensorFlow / Keras
- Google Colab
- Jupyter Notebook

## Repository Structure

```text
OpenCV-Image-Processing-and-CNN/
├── OpenCV_Complete_Colab_Course_Simpsons_GitHub.ipynb
├── README.md
└── Simpsons Dataset/
    └── Uploaded separately when Section 4 is run
```

## Section 1 — OpenCV Basics

I build the foundation for computer vision by working with:

- Image reading and display
- Image dimensions and channels
- Grayscale conversion
- Gaussian blur
- Canny edge detection
- Dilation and erosion
- Image resizing and rescaling
- Drawing lines, rectangles, circles and text
- Video capture and frame processing
- Translation
- Rotation
- Flipping
- Cropping
- Thresholding
- Contour detection

The video examples are adapted for Google Colab. Desktop functions such as `cv.imshow()`, `cv.waitKey()` and `cv.destroyAllWindows()` are not relied on for normal notebook display.

## Section 2 — Advanced OpenCV

I move into more advanced image-processing operations.

### Color Spaces
I work with BGR, RGB, grayscale and HSV representations.

### Channel Operations
I split images into individual channels and demonstrate how channels can be merged again.

### Blurring
I demonstrate smoothing/filtering operations and explain how they affect image noise and detail.

### Bitwise Operations
I demonstrate AND, OR, XOR and NOT operations, which are especially useful when working with masks.

### Masking
I create masks to isolate selected regions of an image.

### Histograms
I analyze pixel-intensity distributions to understand brightness, contrast and channel information.

### Gradients and Edges
I work with Sobel, Laplacian and Canny operations to identify intensity changes and object boundaries.

## Section 3 — Face Detection and Recognition

I demonstrate the difference between face detection and face recognition.

### Haar Cascade Detection
I use a Haar Cascade classifier to locate faces in images.

### LBPH Recognition
I use Local Binary Patterns Histograms (LBPH) for face recognition.

The workflow includes:
1. Preparing training images.
2. Detecting/extracting face regions.
3. Assigning labels.
4. Training the recognizer.
5. Saving the trained model.
6. Loading the model.
7. Performing recognition.

## Section 4 — Simpsons Character Classification CNN

The capstone extends the project from traditional computer vision into deep learning.

My goal is to train a Convolutional Neural Network (CNN) that predicts the Simpsons character represented in an image.

### Dataset

The supplied dataset is organized as:

```text
simpsons/
├── bart_simpson/
├── ...
└── principal_skinner/
```

Each character folder contains image files such as:

```text
pic_0000.jpg
pic_0001.jpg
pic_0002.jpg
...
```

The supplied dataset contains approximately 13,810 images.

### Dataset Handling

I do not require a Kaggle API key. In Google Colab, I upload the dataset ZIP directly through the notebook.

The notebook then:
1. Extracts the ZIP.
2. Finds the `simpsons` directory.
3. Detects the character folders automatically.
4. Counts images in each class.
5. Selects the classes used for the main experiment.
6. Creates a reproducible training/validation split.
7. Builds the TensorFlow input pipeline.

### Preprocessing

I prepare the images by:
- Reading them from disk.
- Converting them to grayscale.
- Resizing them to a fixed input size.
- Normalizing pixel values.
- Assigning numerical class labels.
- Shuffling the dataset.
- Separating training and validation data.

### CNN

I use a CNN because convolutional layers can learn spatial image patterns such as edges, shapes, textures and character-specific features.

The notebook contains the complete TensorFlow/Keras workflow for model construction and training.

### Evaluation

I evaluate the model using:
- Training accuracy
- Validation accuracy
- Training loss
- Validation loss
- Accuracy/loss curves
- Confusion matrix
- Classification report
- Individual image predictions

The notebook does not claim a fixed accuracy before training. Actual results are generated when the notebook is executed.

### Custom Prediction

After training, I can upload my own Simpsons image in Colab and obtain:
- Predicted character
- Model score
- Displayed input image

### Model Saving

The trained model can be saved as:

```text
simpsons_character_classifier.keras
```

and loaded again for later inference.

## Running the Project

1. Open `OpenCV_Complete_Colab_Course_Simpsons_GitHub.ipynb` in Google Colab.
2. Run the setup cells.
3. Work through Sections 1–3.
4. For Section 4, upload the Simpsons dataset ZIP when requested.
5. Run the dataset preparation cells.
6. Train the CNN.
7. Review the accuracy/loss curves.
8. Generate the evaluation metrics.
9. Test individual or custom images.

For CNN training, a Colab GPU runtime is recommended:

```text
Runtime → Change runtime type → GPU
```

## Why the Simpsons Dataset Is Separate

The dataset is large and is intentionally not committed to this GitHub repository. The notebook is designed to accept the ZIP during execution instead.

This keeps the GitHub repository focused on the project code and notebook rather than storing a large image archive.

## Project Flow

```text
Image / Video Input
        ↓
OpenCV Basics
        ↓
Image Processing
        ↓
Advanced OpenCV
        ↓
Face Detection
        ↓
Face Recognition
        ↓
Dataset Preparation
        ↓
CNN
        ↓
Training
        ↓
Validation
        ↓
Evaluation
        ↓
Simpsons Character Prediction
```

## Learning Outcomes

Through this project, I work with both traditional and deep-learning computer vision techniques, including image representation, filtering, morphology, edge detection, thresholding, contours, masking, histograms, video processing, face detection, face recognition, dataset preparation, CNNs, model training and model evaluation.

## Future Improvements

Possible future extensions include:
- Transfer learning with pretrained CNNs.
- Data augmentation.
- More Simpsons character classes.
- Hyperparameter tuning.
- Better class balancing.
- Model interpretability using Grad-CAM.
- Real-time webcam classification.
- A web interface for prediction.
- FastAPI/Flask deployment.
- TensorFlow Lite conversion.

These are future extensions and are not presented as functionality already implemented.

## Author

**Dhrubajyoti**  
BTech — Computer Science & Engineering (AI)

## License

No open-source license has been selected for this repository at this time.
