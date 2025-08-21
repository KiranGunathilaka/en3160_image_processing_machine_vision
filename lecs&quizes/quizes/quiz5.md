# Computer Vision Quiz Study Guide

## Question 1
**How is the solution for the parameters of the line in the Total Least Squares method determined?**

a. By iteratively solving a nonlinear optimization problem.
**b. By finding the eigenvector of the U^T U matrix associated with the smallest eigenvalue.** ✓
c. By finding the largest eigenvalue of the second moment matrix.
d. By using a robust function to minimize the sum of residuals.
e. By selecting a random subset of points and fitting a model.

---

## Question 2
**How many degrees of freedom does a Homography have?**

**a. 8** ✓
b. 3
c. 4
d. 6
e. 9

---

## Question 3
**How many matches are the minimum needed to solve for the parameters of a Homography?**

a. Six
b. Two
c. Three
d. Eight
**e. Four** ✓

---

## Question 4
**In the context of robust alignment, what is the heuristic for rejecting ambiguous matches?**

a. Comparing the color histogram of the patch.
b. Comparing the size of the patch to the size of the feature descriptor.
c. Comparing the number of gradients in each sub-patch.
**d. Comparing the distance of the nearest neighbor to that of the second nearest neighbor.** ✓
e. Comparing the angle of the nearest neighbor to the second nearest neighbor.

---

## Question 5
**In the RANSAC algorithm, what is the role of the inlier threshold t?**

a. To calculate the outlier ratio e.
b. To define the minimum number of points needed to fit a model.
**c. To decide which points are "close" to the fitted model and should be considered inliers.** ✓
d. To determine the number of samples to draw.
e. To set the probability p of success.

---

## Question 6
**In Total Least Squares, what does the parameter (a, b) represent in the line equation ax + by = d?**

a. The second moment matrix.
b. A point on the line.
c. The y-intercept and x-intercept.
d. The slope of the line.
**e. The unit normal to the line.** ✓

---

## Question 7
**What is a Homography?**

**a. A transformation that takes a quad to another arbitrary quad.** ✓
b. A transformation that is specified by only four parameters.
c. A transformation that preserves lengths and angles.
d. A transformation that only includes rotation and translation.
e. A transformation that only works on two cameras with different centers.

---

## Question 8
**What is a key advantage of the SIFT descriptor over using raw pixel intensity vectors?**

a. It is only useful for identifying specific objects.
b. It is a simpler, one-dimensional vector.
c. It is computationally slower.
**d. It is less sensitive to illumination changes.** ✓
e. It is more sensitive to small deformations.

---

## Question 9
**What is a key application of image alignment mentioned in the slides?**

a. Applying artistic filters to images.
b. Compressing image files.
c. Changing the color palette of an image.
**d. Panorama stitching.** ✓
e. Removing noise from photographs.

---

## Question 10
**What is a key disadvantage of the classical Hough Transform that leads to the use of a polar representation?**

a. It cannot handle circles.
b. It is not robust to noise.
c. It requires too many iterations.
**d. The parameter space becomes unbounded and fails for vertical lines.** ✓
e. It is too computationally complex.

---

## Question 11
**What is a key problem with the first attempt at Least Squares Line fitting using the slope-intercept parametrization (y=mx+b)?**

a. It works only for data points that are perfectly collinear.
**b. It is not equivariant with respect to rotation.** ✓
c. It fails for lines with negative slopes.
d. It heavily penalizes inliers.
e. It is computationally inefficient.

---

## Question 12
**What is the basic idea behind voting schemes like the Hough Transform?**

a. To solve a set of linear equations.
b. To randomly sample data points until an outlier-free subset is found.
**c. To let each point vote for all possible models that could have generated it.** ✓
d. To find the most distant point from the model.
e. To find the single best-fitting model in a single iteration.

---

## Question 13
**What is the main difference between "fitting a model to features in one image" and "alignment"?**

a. Alignment is a subset of fitting a model.
b. Fitting a model works on two images, while alignment works on one.
**c. Fitting a model works on features in a single image, while alignment fits a transformation between features in two images.** ✓
d. Alignment is an older technique.
e. Fitting a model is a more computationally expensive process.

---

## Question 14
**What is the main goal of using a robust estimator like RANSAC in image alignment?**

a. To guarantee a perfect fit with no error.
**b. To handle a high percentage of outliers in the set of putative matches.** ✓
c. To reduce the number of initial features detected.
d. To speed up the feature detection process.
e. To find the transformation with the smallest least-squares error.

---

## Question 15
**What is the main problem with using a simple Least Squares fit when an outlier is present in the data?**

**a. It heavily penalizes the outlier due to the squared error, skewing the fit.** ✓
b. It fails to find a solution.
c. It treats the outlier the same as an inlier.
d. It can only be used on two data points at a time.
e. The algorithm becomes computationally expensive.

---

## Question 16
**What is the primary problem that large-scale visual search techniques like vocabulary trees are designed to solve?**

**a. The scalability issue of aligning a test image with a massive database of millions of images.** ✓
b. The problem of having too few images in a database.
c. The problem of images having different resolutions.
d. The computational cost of finding a perfect match between two images.
e. The issue of images being taken from different viewpoints.

---

## Question 17
**What is the primary purpose of "fitting" in image analysis?**

a. To apply Gaussian noise to an image.
**b. To group multiple image features into a more compact, higher-level representation based on a simple model.** ✓
c. To detect edges, corners, and blobs.
d. To reduce the resolution of an image for faster processing.
e. To convert images from color to black and white.

---

## Question 18
**Which of the following is a general approach for robust estimators?**

**a. Finding model parameters that minimize a robust function of the residuals.** ✓
b. Iteratively solving a linear optimization problem.
c. Ignoring all points with a residual greater than a certain threshold.
d. Using only the median of the data points for fitting.
e. Using a slope-intercept parametrization for all lines.

---

## Question 19
**Which of the following is NOT an invariant property of an Affine transformation?**

a. Ratio of lengths on collinear or parallel lines
**b. Length** ✓
c. Ratio of areas
d. Parallelism
e. Linear combinations of vectors

---

## Question 20
**Which of the following is NOT listed as a challenge in the fitting process?**

**a. The computational expense of the algorithm.** ✓
b. Noise in the measured feature locations.
c. Multiple lines in the same image.
d. Missing data due to occlusions.
e. Extraneous data, such as outliers or clutter.

---

## Summary

**Score: 20/20** 🎉

### Key Topics Covered:
- **Total Least Squares (TLS)** - Eigenvector method, unit normal representation
- **Homographies** - 8 degrees of freedom, 4-point minimum, quad-to-quad transformation
- **Feature Matching** - Lowe's ratio test for ambiguous matches
- **RANSAC** - Inlier threshold, robust estimation for outliers
- **SIFT Descriptors** - Illumination invariance
- **Hough Transform** - Voting schemes, polar representation benefits
- **Image Alignment** - Panorama stitching, transformation between images
- **Robust Estimation** - Handling outliers, robust functions
- **Affine Transformations** - Invariant properties (length is NOT preserved)
- **Fitting Challenges** - Data quality issues vs computational concerns

### Study Tips:
1. Focus on understanding the **mathematical foundations** behind each method
2. Remember the **practical applications** and when to use each technique
3. Understand the **trade-offs** between accuracy, robustness, and computational efficiency
4. Pay attention to **invariant properties** of different transformations