# Edge Detection Algorithm

Welcome to the Edge Detection Algorithm project! In this assignment, we will implement edge detection using co-occurrence matrices and integral images.

## Task 1: Edge Detection with Co-occurrence Matrices
- Calculate co-occurrence matrices of an image.
- Nullify (set to 0) the diagonal elements representing pixels with close intensities using a threshold.
- Reconstruct the original image using the nullified co-occurrence matrices.

### Methods
1. `calculateCooccurrence(image)`: Computes co-occurrence matrices.
2. `nullifyPixels(cooccurrenceMatrix, threshold)`: Nullifies pixels within a certain radius of the diagonal.
3. `imgWithCooccurrence(nullifiedMatrices)`: Reconstructs the image.

## Task 2: Edge Detection with Integral Images
- Calculate the integral image of the image.
- Calculate the integral image of the squared version of the image.
- Compute variances of pixel values using integral images and a specified window size.
- Apply a threshold to produce fine edges.

### Methods
1. `integralArray(image)`: Computes the integral image of an image.
2. `localSum(image, topLeft, bottomRight)`: Computes the local sum of a pixel area.
3. `imgWithIntegral(image, windowSize)`: Computes variances and applies thresholding.

## Sample Output Maps
- Top left: Original Image (Gray-Scale)
- Top Right: Integral Image
- Mid Left: Original Image in Gray-Scale squared
- Mid Right: Integral Image
- Bottom Left: Output without thresholding
- Bottom Right: Threshold applied

## Efficiency and Complexity
- Task 1 (Co-occurrence Matrices): The complexity mainly depends on image dimensions and the threshold value. Calculating co-occurrence matrices is O(N^2), while nullifying pixels adds an extra layer of complexity.
- Task 2 (Integral Images): Computing integral images is O(N^2), and calculating variances with a specified window size introduces further complexity.

## Differences in Outputs
Both methods yield edge-detected images, but they may differ in fine details and sharpness. Co-occurrence matrices are more dependent on pixel intensities, while integral images focus on local variances. The choice of method should depend on the specific requirements of your application.
