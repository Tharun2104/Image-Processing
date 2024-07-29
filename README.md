# Image Processing with OpenCV

Welcome to the Image Processing repository! This project showcases various techniques and methods for processing and analyzing images using OpenCV, a popular open-source computer vision library.

## Introduction

In the realm of digital image processing, understanding how images are represented and manipulated is crucial. This repository explores fundamental concepts and provides practical examples to help you get started with image processing using OpenCV.

### Image Representation

Images are essentially two-dimensional data arrays. Regardless of the format or encoding scheme, an image is always represented as one or more two-dimensional arrays, `I(m, n)`, where each element represents a single pixel.

- **Pixel Coordinates**: Traditional matrix notation is used, where horizontal locations are indexed from left to right by the second integer, `n`, and vertical locations are indexed from top to bottom by the first integer, `m`.

### Pixel Values

Pixels in digital images are assigned values that represent their intensity. The intensity values can be stored in different data formats:

- **uint8**: 8-bit unsigned integer (0 to 255)
- **uint16**: 16-bit unsigned integer (0 to 65,535)
- **Double**: Double-precision floating-point (0.0 to 1.0)

### Types of Images

Digital images are categorized into three main types:

- **Binary or Black and White Images**: Represent pixel intensities using only two values (0 for black and 1 for white). Stored as a 2D matrix.

- **Grayscale or Intensity Images**: Represent a range of gray intensities from black to white. Stored as a 2D matrix.

- **RGB or Color Images**: Represent the intensity of each primary color (Red, Green, Blue) at each pixel. Stored as a 3D matrix where the third dimension has a size of 3 (one for each color channel).

### OpenCV’s Color Channel Order

When using OpenCV’s `imread()` function to load color images, be aware that the default color channel order is BGR (Blue, Green, Red), not RGB. This means:

- The `imread()` function returns a 3D numpy array for color images.
- Dimensions are typically `(height, width, 3)`, with:
  - Channel 0: Blue
  - Channel 1: Green
  - Channel 2: Red

This BGR order is specific to OpenCV and differs from the RGB format used by many other libraries. To convert to RGB format for compatibility or display, use OpenCV’s `cvtColor()` function.
