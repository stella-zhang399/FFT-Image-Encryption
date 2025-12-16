# FFT-Image-Encryption
FFT-based image decryption system. Reconstructs scrambled images by implementing a custom inverse block permutation algorithm on the centered Fourier spectrum and applying iFFT.

## Project Goal and Context
This project focuses on the core mechanics of image encryption through frequency domain scrambling. The objective was to develop and implement a generalized decryption algorithm capable of reversing a multi-block permutation applied to a centered image Fourier matrix. The process involves reconstructing the original image from its scrambled spectral components, demonstrating proficiency in scientific computing techniques for data security and image recovery.

## Methodology & Implementation
The core task required engineering an algorithm that performed three sequential operations on the input Fourier Matrix ($320 \times 320$):

* Inverse Block Permutation: A crucial step involving mapping 16 discrete $20 \times 20$ blocks, located at the center of the Fourier matrix, back to their original placement using a supplied inverse permutation vector (the decryption key).

* Frequency Shift: Implemented the necessary shifting of the Fourier matrix from the zero-frequency-at-center convention (used for visualization) to the corner-based convention required by the standard Inverse Fast Fourier Transform (iFFT) function.

* Image Reconstruction: Applied the Inverse Fast Fourier Transform (iFFT) to the corrected and unpermuted spectral matrix to reconstruct the original spatial image data. The algorithm was designed to be platform-independent and robust enough to handle arbitrary $N \times N$ centered Fourier matrices and permutation keys of varying size and complexity.

## Key Results and Accomplishments
* Algorithm Development: Developed a robust permutation engine that successfully maps scattered spectral blocks back to their original coordinates based on an inverse permutation key, achieving full data recovery.

* Data Structure Manipulation: Engineered efficient matrix logic to handle the multi-dimensional slicing, shifting, and reassembly of the $320 \times 320$ Fourier matrix in the frequency domain.

* Image Recovery: The final output successfully reconstructed the image matrix, validating the accuracy of the frequency shifting and inverse permutation logic.
