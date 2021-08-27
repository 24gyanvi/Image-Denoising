# Image-Denoising
In this project noisy images are denoised using deep learning and python.
<br/>Link to noisy input datasetof 2429 images:https://drive.google.com/drive/folders/1g-LJV28jfkbFzJK6fxCK-ycabzhNb9_X?usp=sharing
<br/>Link to taget dataset of 2429 images:https://drive.google.com/drive/folders/1K0DNN4wg-Z_98MWaKVyqrM1LHamF-V1B?usp=sharing
<br/>Link to the original dataset of 7199 images which is a merging of GoPro, HIDE, RealBlur_J and RealBlur_R: https://drive.google.com/drive/folders/1BzzTN--C3TNITDr5HRXA6AnYk61rr3Nc?usp=sharing
# Results
![noisy](https://user-images.githubusercontent.com/88244007/131150651-916eba85-333b-4ae7-ac6d-c8b4afc15933.png)
![corrected](https://user-images.githubusercontent.com/88244007/131150647-04a04341-7686-463c-8f35-141149ce50c4.png)
![ground truth](https://user-images.githubusercontent.com/88244007/131150639-a5cdfcee-2d5f-49fc-b32a-04e5a6910457.png)
<br/> &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Noisy image &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Corrected image &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; Ground truth
# Method
<br/> The first step was to convert coloured images into greyscale and to a size of 100 X 100 and then introduce salt and pepper noise by randomly picking up pixels and coloring them black and white. Then both ground truth images and noisy images were stored inseparate folders. For more details visit Introducing_salt_and_pepper_noise.ipynb and the links to the datsets are given above.
<br/>
<br/>Now the first step of denoising was to first randomly import both input and target images images and convert them to numpy array and store them in a list. Then train-test split was made in the ratio of 4:1. Out of training dataset 10% is passed for validation. Then using autoencoders model, training is done over train dataset and random testing is done over test dataset which can be seen in Salt_and_pepper_denoising.ipynb 
