# Convolution Operators

## Naïve
This method describes element-wise multiplication or direct computation. An overview, the kernel slides over the image and performs the direct element-wise multiplication. The products from these calculations are summed to produce each element of the output feature map.

## im2col
The im2col algorithm relates to matrix multiplication as it transforms the convolution operation by rearranging the overlapping image patches into columns of a matrix. These overlapping paths are the regions covered by the kernel. 

## Fast Fourier Transform (FFT)
This convolution method falls under the transform methodology where both the input image and the kernel are transformed into the frequency domain using the Fourier transform. Convolution is carried out by performing element-wise multiplication in this domain, exploiting convolution theorem.