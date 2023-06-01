# Team Introduction
- Name: 이승준(202211337) 
- Github ID: somniumcaeruleumKonkuk 
- Team type: Individual

# Topic Introduction
- Deep cnn 기술을 이용한 Image Denoising
- Source code: https://github.com/wbhu/DnCNN-tensorflow

# Results

Test Set


Noised Image 1

<img width="90" alt="noised" src="https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/9361221d-63ef-4ebc-b2c0-970a3a465f1d">


Denoised Image 1

![denoised](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/8d13f1e9-8d4d-4436-aae6-605cb57f1632)


Comparing between noised, denoised

<img width="272" alt="compare1" src="https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/50e439f2-2ffa-46b8-a2b0-1ba3e68fc260">


Noised Image 2

![noised1](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/db26d598-ed5e-43ea-9d11-1a3a0bba7fa8)


Denoised Image 2

![denoised2](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/dc851122-0fd6-4e96-b442-f43664942c9d)


Comparing between noised, denoised

<img width="280" alt="compare2" src="https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/b9edd589-5287-44bc-987c-3eda07a3c556">


# Analysis/Visualization
- (currently empty)

# Installation
- Install numpy, opencv, tensorflow.

## Environment: 
    Numpy version: 1.23.5
    Opencv version: 4.7.0
    Tensorflow version: 2.12.0
    OS: Windows 11 Education (the latest version in 6/1/2023)
    
## Data preprocessing and noise generation
"
Before training, you have to rescale the images to 180x180 and adding noise to them.
The folder structure is supposed to be:
```
./data/train/original  for the 180x180 original train images
./data/train/noisy  for the 180x180 noisy train images
./data/test/original  for the 180x180 original test images
./data/test/noisy  for the 180x180 noisy test images
```
You need the original files for testing just to calculate the PSNR.
You can denoise without original files: just put the noisy files also in ./data/test/original
" - https://github.com/wbhu/DnCNN-tensorflow

## How to Train
```
./data/train/original  put the 180x180 original train images here
./data/train/noisy  put the 180x180 noisy train images here
```

- Put the images at the right places
- Start cmd
- Move to the directory that the main.py exists using cd command
- Enter the command below.
```
python main.py
```

## How to Test
```
./data/test/original put the 180x180 original test images here *it's totally ok to put the same image here
./data/test/noisy  put the 180x180 noisy test images here 
```

- Put the images at the right places
- Start cmd
- Move to the directory that the main.py exists using cd command
- Enter the command below.
```
python main.py --phase test
```

# Presentation
- (currently empty)
