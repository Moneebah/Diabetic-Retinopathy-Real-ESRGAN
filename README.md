# Enhancing Diabetic Retinopathy Images Using Transfer Learning with Fine-Tuned Real-ESRGAN

Using Real-ESRGAN to enhance real hospital data


![image](https://github.com/Moneebah/Diabetic-Retinopathy-Real-ESRGAN/assets/129015993/53b05045-a7f7-4c56-938b-bc5726f57241)
![image](https://github.com/Moneebah/Diabetic-Retinopathy-Real-ESRGAN/assets/129015993/bcbcbc58-c876-4d4e-9551-950f59c1ca54)

[images are very close examples of the real hospital data]


# Introduction:
Fine-tuned the state-of-the-art Real-ESRGAN model (by [xinntao](https://github.com/xinntao/Real-ESRGAN)) on images of diabetic retinopathy. Using transfer learning, this optimized model was then applied to real hospital data. The primary motivation behind this project was to tackle the challenges associated with real hospital datasets. Even though these datasets often have large image dimensions (around 3000 pixels in width), they frequently suffer from compromised pixel quality.

# Objective:
The primary objective was to achieve a high-resolution output where the intricate details of the blood vessels and other crucial features in retinal images are preserved and enhanced. This not only aids in better visualization but also potentially offers more accurate diagnostic insights.

# Methodology:
## 1. Data Source:
Employed the [Kaggle's diabetic retinopathy dataset](https://www.kaggle.com/datasets/tanlikesmath/diabetic-retinopathy-resized), which has good pixel quality, as the baseline for fine-tuning.

## 2. Fine-Tuning:
Real-ESRGAN was then fine-tuned on this dataset, capitalizing on its high-quality pixel images. The training process spanned over 3,500 iterations for just 1 epoch, given the substantial size of the dataset (30,000+ images).

## 3. Application:
The fine-tuned model was subsequently applied to the real hospital dataset. This dataset, characterized by its vast image dimensions but compromised pixel quality, exhibited noticeable noise upon zooming in. However, with the application of the fine-tuned Real-ESRGAN,  significant improvements were observed in the image details, with a notable reduction in noise.

## 4. Optimal Size Resolution:
Through experimentation, it was discerned that the best results were obtained by resizing the images from their original dimension (around 3000 pixels) to 1024 pixels. This resize operation, followed by the application of the fine-tuned model on the real data, yielded the most optimal results.

# Results:
The results were quite promising. The fine-tuned model adeptly addressed the noise and quality limitations of the real hospital dataset by producing images with enhanced clarity. Specifically, the details of blood vessels, which are paramount in diagnosing and studying diabetic retinopathy, were significantly more defined and visible.

# Usage

Clone this repository and follow the steps mentioned in file: `finetuned-retinopathy-model-usage-guide (1).ipynb` to apply this finetuned model onto your own dataset

# Conclusion:
Fine-tuning advanced models like Real-ESRGAN on specialized datasets can dramatically improve the quality of medical images, particularly when the original data suffers from noise and other quality issues. Such advancements not only facilitate clearer visualizations for medical practitioners but could also lead to more precise diagnostic methodologies in the future.




