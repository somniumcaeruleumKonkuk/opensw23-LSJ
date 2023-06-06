# Team Introduction
- Name: 이승준(202211337) 
- Github ID: somniumcaeruleumKonkuk 
- Team type: Individual

# Topic Introduction
- Deep cnn 기술을 이용한 Image Denoising
- Source code: https://github.com/wbhu/DnCNN-tensorflow

# Results
## Original Image
<img width="92" alt="original2" src="https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/157664a0-728d-4918-bde9-4a72437d7ba5">

- Image Source: https://www.nationalgeographic.com/adventure/article/140127-cats-pets-animals-nation-dogs-people-science
- PHOTOGRAPH BY FSTOP, ALAMY

## Noised Image
![testSet1](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/b7fff828-8f33-4a83-b563-3c7d632710c6)

- I added noises to the original image using https://pinetools.com/add-noise-image.
- Amount of Noise: 50
- Strength of the noise: 50
- Monochromatic: False

## Denoised Image
![0000](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/4a2684a7-23ae-40ac-a080-33b39c020b32)


# Analysis/Visualization
## Test Set
- I added noises to the original image using https://pinetools.com/add-noise-image.

### Original Image
![original1](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/3100bc8c-3135-447d-aa15-61cd55160e59)
- Image Source: https://commons.wikimedia.org/wiki/File:Cat03.jpg

### Image 1
![1_020](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/f645db63-501f-4221-b0b8-6d5cceb61671)
- Amount of Noise: 50
- Strength of the noise: 20
- Monochromatic: False

### Image 2
![1_040](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/71f9c002-0394-40fb-882b-0a4f2ccbc023)
- Amount of Noise: 50
- Strength of the noise: 40
- Monochromatic: False

### Image 3
![1_060](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/18245c41-57b5-493a-8844-2bf618815b51)
- Amount of Noise: 50
- Strength of the noise: 60
- Monochromatic: False

### Image 4
![1_080](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/5d604778-c3d0-40e2-9e69-dccedf744db1)
- Amount of Noise: 50
- Strength of the noise: 80
- Monochromatic: False

### Image 5
![1_100](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/a56c7e90-fb09-46ba-9e0a-7e8092425197)
- Amount of Noise: 50
- Strength of the noise: 100
- Monochromatic: False

### Image 6
![1_100_grey](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/54412271-e5e4-4476-96e5-6a07433f6af0)
- Amount of Noise: 50
- Strength of the noise: 100
- Monochromatic: True

## Denoised Images

### Image 1
![0000](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/97adde7e-ae6c-4a3a-9684-ac7543b78802)

### Image 2
![0001](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/16cd86a2-b3f1-4547-8b8c-7d866a64a637)

### Image 3
![0002](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/81b554d6-6bbc-4b3b-bebc-b3015559246b)

### Image 4
![0003](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/54cf5115-518a-4677-a15e-58bf71e4cc6d)

### Image 5
![0004](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/f08ac3db-71e5-41fd-ae97-d25058c3f738)

### Image 6
![0005](https://github.com/somniumcaeruleumKonkuk/opensw23-LSJ/assets/127181476/7deb86e1-e670-414c-9acf-ef27ff85b322)


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
