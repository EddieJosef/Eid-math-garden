# Math Garden

Math Garden is a web application that allows users to draw hand-written digits on a canvas. The application uses JavaScript and various libraries to recognize and process the drawn digits. The recognized digits are then treated with OpenCV.js to convert them into images compatible with a neural network model designed with TensorFlow. The model predicts the digit and compares it to the actual input. If the prediction is correct, a garden will grow on the website. If the prediction is wrong, the garden will wither.

## Getting Started

To use Math Garden, follow these steps:

1. Clone the repository to your local machine.
2. Open the `index.html` file in a web browser.
3. Draw a digit on the canvas using your mouse or touch input.
4. Click the "Recognize" button to process the drawn digit.
5. The model prediction will be displayed on the screen.
6. If the prediction is correct, a garden will grow. If it is wrong, the garden will wither.

## Prerequisites

To run Math Garden, you need the following prerequisites:

- A web browser with JavaScript support.
- TensorFlow.js library
- OpenCV.js library

Ensure that you have the necessary dependencies installed before running the application.

## Usage

The main JavaScript code for the digit recognition and image processing can be found in the `script.js` file. The `loadModel` function loads the TensorFlow.js model from the `TFJS/model.json` file.

The `predictImage` function is responsible for processing the drawn digit on the canvas. It performs the following steps:

1. Converts the image to grayscale.
2. Applies a binary threshold to the image.
3. Finds contours in the image.
4. Extracts the digit region from the image using the bounding rectangle of the contour.
5. Resizes the digit region to a standard size of 20x20 pixels.
6. Centers the digit within a 28x28 pixel canvas.
7. Converts the pixel values to a Float32Array and scales them.
8. Creates a TensorFlow tensor from the scaled pixel values.
9. Passes the tensor through the loaded model for prediction.
10. Prints the prediction result to the console and returns the output.

Please note that the code includes commented-out console logs and testing lines, which can be uncommented and used for debugging or visualizing intermediate results.

## Contributing

Contributions to Math Garden are welcome! If you have any ideas, improvements, or bug fixes, feel free to open an issue or submit a pull request on the GitHub repository.
