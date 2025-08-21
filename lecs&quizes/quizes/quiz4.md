# Computer Vision Quiz - Study Guide

**Score: 18/20**

---

## Question 1
**In blob detection, if σ = 14, what is the radius of the blob that gives the maximum response?**

**Answer:** r = σ√2 = 14√2 ≈ **19.8 pixels**

---

## Question 2
**Harris corner detection is NOT invariant to:**

a. Image scaling ✅ **CORRECT**
b. Image rotation
c. All of the above
d. Image translation
e. Affine intensity change

**Explanation:** Harris is invariant to translation, rotation, and affine intensity changes, but NOT to scaling.

---

## Question 3
**In a derivative filter, the sum of filter values should be:**

a. Zero ✅ **CORRECT**
b. Greater than one
c. One
d. Less than zero
e. Infinity

**Explanation:** Derivative filters must sum to zero to respond to changes but not constant values.

---

## Question 4
**In a smoothing filter such as Gaussian, the sum of the filter values should be:**

a. Greater than one
b. Infinity
c. Less than zero
d. Zero
e. One ✅ **CORRECT**

**Explanation:** Smoothing filters sum to 1 to preserve image brightness.

---

## Question 5
**In discrete images, partial derivatives can be approximated using:**

a. Color histograms
b. Hough transform
c. Finite differences ✅ **CORRECT**
d. Fourier transforms
e. Principal component analysis

**Explanation:** Finite differences are the standard discrete approximation of continuous derivatives.

---

## Question 6
**In Harris corner detection, the second moment matrix is computed over:**

a. Only corner pixels
b. Gradient magnitude image
c. A fixed rectangular window
d. A Gaussian window around each pixel ✅ **CORRECT**
e. The entire image

**Explanation:** Harris uses Gaussian weighting for smooth, localized computation around each pixel.

---

## Question 7
**In hysteresis thresholding of Canny edge detection, the low threshold is used to:**

a. Continue edge curves from strong edges ✅ **CORRECT**
b. Start new edges
c. Eliminate all weak edges
d. Determine edge orientation
e. Reduce noise

**Explanation:** Low threshold allows weak edges to be kept if connected to strong edges, continuing edge curves.

---

## Question 8
**In SIFT, detection is __________ and description is __________.**

a. separable; inseparable
b. covariant; invariant ✅ **CORRECT**
c. isotropic; anisotropic
d. invariant; covariant
e. linear; nonlinear

**Explanation:** Detection is covariant (transforms with the image), description is invariant (remains stable).

---

## Question 9
**In the Canny edge detector, non-maximum suppression is used to:**

a. Reduce thick ridges to single-pixel edges ✅ **CORRECT**
b. Increase gradient magnitude
c. Remove low-frequency noise
d. Link broken edges
e. Normalize gradient orientation

**Explanation:** NMS thins thick edge responses to precise single-pixel edges.

---

## Question 10
**Scale normalization in Laplacian-based blob detection involves multiplying by:**

a. σ² ✅ **CORRECT**
b. 1/σ
c. √σ
d. σ
e. log(σ)

**Explanation:** σ² normalization compensates for the 1/σ² scaling behavior of the Laplacian.

---

## Question 11
**The characteristic scale of a blob is defined as:**

a. The smallest scale used in convolution
b. The scale at which the Laplacian response is smallest
c. The average of all detected scales
d. The largest scale used in convolution
e. The scale that produces the peak Laplacian response at the blob center ✅ **CORRECT**

**Explanation:** Characteristic scale is where the blob achieves maximum response, indicating optimal size matching.

---

## Question 12
**The derivative theorem of convolution states that:**

a. Differentiation is convolution, and convolution is associative
b. Differentiation and convolution are commutative ✅ **CORRECT**
c. Differentiation is not possible in the frequency domain
d. Differentiation removes noise
e. Convolution can replace differentiation entirely

**Explanation:** ∂/∂x [f * g] = (∂f/∂x) * g = f * (∂g/∂x) - order can be swapped.

---

## Question 13
**The difference of Gaussians (DoG) is used because:**

a. It normalizes intensity values
b. It sharpens the image
c. It approximates the Laplacian efficiently ✅ **CORRECT**
d. It reduces noise without blurring edges
e. It detects edges only

**Explanation:** DoG provides a computationally efficient approximation to the Laplacian of Gaussian.

---

## Question 14
**What is the primary goal of edge detection in an image?**

a. Remove noise from the image
b. Increase image contrast
c. Reduce image size
d. Enhance colors
e. Identify sudden changes in image intensity ✅ **CORRECT**

**Explanation:** Edges correspond to locations of rapid intensity change in images.

---

## Question 15
**Which factor does NOT contribute to the robustness of SIFT descriptors?**

a. Ability to handle day vs. night lighting changes
b. Exact photometric invariance
c. Ability to handle up to ~60° out-of-plane rotation
d. Availability of open-source implementations
e. Real-time performance ✅ **CORRECT**

**Explanation:** Performance speed doesn't affect robustness; robustness is about stability under transformations.

---

## Question 16
**Which mathematical operator is primarily used in blob detection?**

a. Roberts operator
b. Sobel operator
c. Laplacian of Gaussian ✅ **CORRECT**
d. Discrete cosine transform
e. Hough transform

**Explanation:** LoG is the fundamental operator for blob detection due to its second-order derivative properties.

---

## Question 17
**Which of the following is NOT a common cause of edges in images?**

a. Compression artifacts
b. Uniform background ✅ **CORRECT**
c. Object boundaries
d. Illumination changes
e. Texture changes

**Explanation:** Uniform backgrounds have constant intensity with no sudden changes, hence no edges.

---

## Question 18
**Which of the following is TRUE for affine adaptation in feature detection?**

a. It cannot handle scaling
b. It only works for spherical objects
c. It handles viewpoint changes for planar objects under orthographic projection ✅ **CORRECT**
d. It eliminates noise completely
e. It is invariant to all 3D rotations

**Explanation:** Affine adaptation compensates for affine transformations from viewpoint changes of planar surfaces.

---

## Question 19
**Which property of a good feature ensures it can be found despite scaling, rotation, and lighting changes?**

a. Efficiency
b. Saliency
c. Locality
d. Repeatability ✅ **CORRECT**
e. Compactness

**Explanation:** Repeatability ensures the same features are consistently detected across different conditions.

---

## Question 20
**Which step eliminates rotational ambiguity in SIFT descriptors?**

a. Histogram of gradient orientations ✅ **CORRECT**
b. Non-maximum suppression
c. Gaussian smoothing
d. Laplacian normalization
e. Harris corner detection

**Explanation:** The orientation histogram finds dominant directions to establish a canonical orientation reference.

---

## Key Concepts Summary

### Harris Corner Detection
- **Invariant to:** Translation, rotation, affine intensity changes
- **NOT invariant to:** Scaling
- Uses Gaussian window for second moment matrix computation

### SIFT Features
- **Detection:** Covariant (transforms with image)
- **Description:** Invariant (stable across transformations)
- **Rotation invariance:** Achieved through orientation histogram
- **Robustness factors:** Lighting changes, photometric invariance, viewpoint tolerance

### Edge Detection
- **Goal:** Identify sudden intensity changes
- **Canny steps:** Gaussian smoothing → gradients → non-maximum suppression → hysteresis
- **NMS:** Reduces thick ridges to single-pixel edges
- **Hysteresis:** Low threshold continues edges from strong edges

### Blob Detection
- **Primary operator:** Laplacian of Gaussian (LoG)
- **Scale normalization:** Multiply by σ²
- **Characteristic scale:** Scale producing peak response
- **DoG approximation:** Efficient alternative to LoG

### Filter Properties
- **Derivative filters:** Sum to zero
- **Smoothing filters:** Sum to one
- **Convolution theorem:** Differentiation and convolution commute