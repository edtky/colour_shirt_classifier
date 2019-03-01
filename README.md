# Coloured Shirt Classification

Using ImageAI to custom train a classifier to differentiate between images containing different coloured shirts.

**Findings:**

It turns out that most pre-trained CNNs don't have very good color-sensitive filters, because shapes and edges (rather than color) was a more decisive factor in recognizing natural objects.

To detect shirts of a specific color, we may need to break the problem down into 2 tasks: color recognition then object recognition.


# Steps to train a custom classifier using ImageAI:

1. Scrap training images from Google using 'googledownloadimage'.
    - https://github.com/hardikvasa/google-images-download
    - Be sure to clean your train set - it makes alot of difference!
    
2. Train custom classifier using ImageAI
    - https://github.com/OlafenwaMoses/ImageAI/blob/master/imageai/Prediction/CUSTOMTRAINING.md
    - Recommendation: >500 training examples per class, >100 testing examples per class
    
3. Predict unseen images using trained classifier
    - https://github.com/OlafenwaMoses/ImageAI/blob/master/imageai/Prediction/CUSTOMPREDICTION.md
    - Choose the best model from training by looking at accuracy


