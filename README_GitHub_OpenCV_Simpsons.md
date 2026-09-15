# OpenCV with Python — Complete Google Colab Course

This repository contains my Colab-ready OpenCV course project, including:

- OpenCV basics
- Advanced OpenCV
- Face detection and recognition
- Simpsons character classification with a CNN

## Simpsons dataset

The Simpsons image dataset is **not committed to this repository** because the supplied ZIP is about 332 MB and contains approximately 13,810 images. GitHub's normal repository/file limits make committing that dataset directly unsuitable.

The notebook is already prepared to accept the dataset ZIP in Google Colab.

### To run

1. Upload `OpenCV_Complete_Colab_Course_Simpsons_GitHub.ipynb` to GitHub.
2. Open the notebook in Google Colab.
3. Run the setup cells.
4. When Section 4 asks for the dataset, upload the supplied Simpsons ZIP.
5. The notebook automatically extracts the ZIP, finds the `simpsons/` directory, selects the ten largest character classes, prepares the TensorFlow pipeline, trains the CNN, evaluates it, and supports custom-image prediction.

No Kaggle API key is required.
