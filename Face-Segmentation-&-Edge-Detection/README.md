# Face Segmentation & Edge Detection

This project demonstrates the application of edge detection and face segmentation techniques using Python and OpenCV. The goal was to capture facial features while applying edge detection methods and minimizing noise. All tasks were performed on **Google Colab** to ensure accessibility and ease of experimentation.

## Key Techniques Used:

### 1. **Edge Detection Methods:**
- **Sobel Edge Detection:**  
  The Sobel operator was used to compute gradients along the X and Y axes separately, then combined to highlight edges in the image. This method focused on detecting fine facial features along with the edges.
  
- **Canny Edge Detection:**  
  The Canny edge detector was applied to the preprocessed image using optimal thresholds of 40 (low) and 135 (high) to extract facial edges while maintaining a minimal level of noise.

- **Custom Edge Detection Function:**  
  A custom Python-based edge detection function was developed using `gaussian_laplace` for smoothing and `convolve` for edge detection. The gradient magnitude was compared to threshold values to identify edges, with further tuning needed for optimal results.

### 2. **Segmentation Using KMeans Clustering Algorithm:**
- **Segmentation Approach:**  
  The image was divided into distinct color clusters, and a KMeans algorithm was applied to segment the image. The segmented image was divided into 5 clusters, allowing the face and background to be clearly differentiated. The background was changed to black, while the facial areas were labeled with distinct colors (e.g., hair in blue and the rest of the face in red).

### 3. **Image Preprocessing:**
- **Image Upload:**  
  The image was read and processed using OpenCV's `cv2.imread` for reading the file and `cv2.cvtColor` to convert the image to grayscale.
  
- **Noise Reduction:**  
  The `cv2.filter2D()` function was applied with a 5x5 averaging kernel to reduce noise, smoothing the image for better edge detection results.

## Results:

- The **Sobel** and **Canny** edge detectors successfully highlighted the edges of facial features, with the Canny detector producing a cleaner result with minimal noise.
- The **Custom Edge Function** yielded satisfactory edge detection but requires further tuning to improve accuracy.
- The **KMeans Segmentation** divided the face into distinct areas, helping to separate the facial features from the background effectively.

## Future Improvements:
- Fine-tune the custom edge detection method for better accuracy.
- Experiment with additional clustering techniques or segmentation algorithms for improved facial feature segmentation.

## Environment:
This project was performed on **Google Colab**, utilizing Python and OpenCV. To run this code, you can either upload your own image or use the provided datasets and run the cells in a Google Colab notebook.