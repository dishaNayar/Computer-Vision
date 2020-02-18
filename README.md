# Computer-Vision
Basic computer vision problems solved using matlab 

Files and their description 

1. Bilateral_Filtering.mlx
  Implementation of Bilateral Filtering in Matlab 
  Approach followed :
  1. I am using an 11*11 kernel for smoothing.
  2. The image is sliced using matrix manipulation based on the kernel size
  3. Iterating over the complete image to calculate the output image
  
2. Camera_Calibration.mlx
  Camera Calibration to find its intrinsic and extrinsic parameters
  
3. Fourier_Transform.mlx
  Magnitude and Phase reconstruction of images (using Fourier transforms)
  
4. GenerateNewPerspectives.mlx
  Undistort an image using homography and generate new perspectives (first part is in file UndistortImage.mlx)
  
5. Image_Blending.mlx
  Image Blending using Pyramids 
  Approach Followed :
  1. The reduce function is called ‘GaussianPyramid’. The image is blurred using ‘imgaussfilt’ function of matlab. To down sample the        image by a factor of 2, every second row and column of the image is convolved with a Binomial Filter.
  2. The Expand function uses zero stuffing to increase the size of the images and is then convolved with an interpolating bilinear          kernel.
  3. The function ‘LaplacianPyramid’ is used to calculate the different image levels in the Laplacian image. It calls the expand              function to expand the image and then takes the difference between images.
  4. ‘GauLapWithMask’ function is used to multiply the gaussian pyramid levels of mask and maskinv with the corresponding Laplacian           pyramids of the face and hand images respectively.
  5. The final pyramid is collapsed to get the blended image.

6. RotatingImage.mlx 
  Rotate an Image in Matlab without using the inbuilt function.
  Approach followed :
  1. The four corners of the original Image are used to calculate the height and the width of the rotated image by using rotation            matrix.
  2. The new image is assigned all zero values.
  3. Itterate over the zero image and apply rotation inverse matrix to get the corresponding coordinate in the original image.
  4. If the point is found on the original image, the corresponding point in the zero image is replaced with the original image’s pixel      value.
  5. The above method is used to prevent holes from generating while rotating an image.

7. UndistortImage.mlx
  Undistort an image using homography and generate new perspectives (second part is in file GenerateNewPerspectives.mlx)


