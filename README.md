# Neural Network for Multi-Class Handwritten Character Recognition

This project implements a custom neural network from scratch to classify grayscale images of alphanumeric characters into **62 classes**, comprising digits (`0-9`), uppercase letters (`A-Z`), and lowercase letters (`a-z`). The neural network is trained using **backpropagation** and optimized with **gradient descent**, showcasing foundational principles of deep learning.

---

## Features
- **Custom Neural Network**:
  - 3-layer architecture with input, hidden, and output layers.
  - **Sigmoid activation function** for non-linear learning.
  - Optimized with **Xavier initialization**, **gradient clipping**, and **mini-batch processing**.
- **Performance Metrics**:
  - Achieved a **training accuracy of 67.42%** and a **testing accuracy of 43.55%**.
- **Robust Training**:
  - Trained for 2,000 epochs with a learning rate of 0.01 and a batch size of 32.
- **Dataset Processing**:
  - Images resized to `80x60 pixels` and normalized for efficient computation.

---

## Dataset Overview
- **Structure**:
  - Organized into 62 folders (`Sample001` to `Sample062`), with each folder containing images of one class.
- **Classes**:
  - `Sample001` to `Sample010`: Digits (`0-9`).
  - `Sample011` to `Sample036`: Uppercase letters (`A-Z`).
  - `Sample037` to `Sample062`: Lowercase letters (`a-z`).
- **Preprocessing Steps**:
  1. **Image Loading**: Loaded using Python Imaging Library (PIL).
  2. **Grayscale Conversion**: Simplified images for consistent input.
  3. **Resizing**: Resized all images to `80x60 pixels`.
  4. **Normalization**: Scaled pixel values to `[0, 1]`.
  5. **Flattening**: Converted images into vectors of size `4,800` (`80x60`).
  6. **Label Encoding**: Assigned numeric labels to each class.
- **Data Splitting**:
  - **Training Set**: 50 images per class.
  - **Testing Set**: 5 images per class.

---

## Neural Network Architecture
- **Input Layer**:
  - **Size**: 4,800 neurons (one for each pixel in the image vector).
- **Hidden Layer**:
  - **Size**: 100 neurons.
  - **Activation Function**: Sigmoid.
- **Output Layer**:
  - **Size**: 62 neurons (one for each class).
  - **Activation Function**: Sigmoid.
  - **Output**: A vector of probabilities indicating the likelihood of each class.

---

## Results
- Training Accuracy: 67.42%
- Testing Accuracy: 43.55%

---

## Challenges and Optimizations
- **Vanishing Gradients:**
  - Addressed by using Xavier initialization to stabilize weight updates.
- **Gradient Explosions:**
  - Mitigated by implementing gradient clipping to restrict gradient magnitudes.
- **Convergence:**
  - Improved with mini-batch processing, stabilizing updates and reducing noise.

---

## Future Enhancements
- Explore ReLU activation functions to mitigate vanishing gradients.
- Experiment with convolutional neural networks (CNNs) for feature extraction.
- Implement advanced optimization techniques like Adam optimizer for faster convergence.
- Evaluate on larger and more diverse datasets.
