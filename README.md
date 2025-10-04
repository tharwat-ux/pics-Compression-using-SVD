# Image Compression using SVD
===============================

## Overview
-----------
This project implements **image compression** using **Singular Value Decomposition (SVD)**.  
The main idea is to reduce the storage space of an image by keeping only the most important singular values, while still maintaining most of the visual quality.

--------------------------------------------------------------------------------------------

## Algorithm / Steps
---------------------
1. **Load the Image**  
   Read the image in grayscale (or RGB if needed).

2. **Convert Image to Matrix**  
   Represent the image as a 2D matrix where each entry is a pixel intensity.

3. **Apply SVD**  
   Decompose the image matrix `A` into three matrices: {A = U @ S @ V^T}  
   - `U` and `V^T` are orthogonal matrices.  
   - `S` is a diagonal matrix containing singular values (importance of each component).

4. **Select Top K Components**  
   Keep only the top `K` singular values that explain the desired amount of information (e.g., 90–95% of variance).  
   This reduces storage significantly.

5. **Reconstruct Compressed Image**  
   Multiply the truncated matrices back to get the compressed image:  
   {
   A_{compressed} = U_k @ S_k @ V_k^T
   }

6. **Compute Compression Rate**  
   Compare the size of the original image and the compressed version:  

7. **Visualize Results**  
   Show the original image, compressed image, and optionally the difference image to see the quality loss.

--------------------------------------------------------------------------------------------
