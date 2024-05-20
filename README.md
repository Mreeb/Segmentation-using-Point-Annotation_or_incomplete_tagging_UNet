# Exploring Factors Affecting Remote Sensing Image Segmentation using only few points instead of full masks.

## Introduction
Welcome to my exploration of the challenges in segmenting remote sensing images. Here, I delve into the impact of two critical factors: point annotation density and contrast enhancement. The focus is on understanding how these factors influence the accuracy of segmentation models, particularly in identifying water bodies.

## Methodology
For this assessment, I employed a UNet architecture for segmentation, incorporating custom encoder and decoder blocks. The model training utilized the Adam optimizer with a learning rate of 0.001 and binary cross-entropy loss. The investigation revolved around:

### Point Annotation Density
Experimenting with various densities of point annotations, ranging from 50 to 200 points per image.

### Contrast Enhancement
Exploring the effects of contrast enhancement techniques on segmentation accuracy through preprocessing input images.

## Experimental Process

### Purpose/Hypothesis

- **Point Annotation Density:** Suspecting that a higher density of points could enhance the model's spatial understanding, potentially leading to improved accuracy.
- **Contrast Enhancement:** Believing that enhancing contrast could aid the model in better distinguishing water bodies from surrounding features.

### Experiment 1: Point Annotation Density

- **Process:** Generating point labels from full segmentation masks and varying the number of points per image.
- **Results:** Training the model with different densities of point annotations revealed a positive correlation between point density and segmentation accuracy, with higher densities yielding better results.

### Experiment 2: Contrast Enhancement

- **Process:** Implementing contrast enhancement techniques like histogram equalization on input images.
- **Results:** The model displayed improved accuracy when trained on contrast-enhanced images compared to the baseline, indicating that enhanced contrast assists the model in sharper segmentation of water bodies.

## Conclusion
In conclusion, both point annotation density and contrast enhancement emerge as crucial factors in remote sensing image segmentation. Increased point density enhances accuracy, while contrast enhancement significantly improves the model's ability to discern features. These findings are pivotal for optimizing segmentation models for real-world applications.

## Future Directions
Looking ahead, I aim to delve into additional factors influencing segmentation performance, including the distribution of point annotations and the integration of advanced data augmentation techniques. Furthermore, testing the robustness of these techniques across diverse environmental conditions and datasets will provide more comprehensive insights.

## Results
Below are the results from the experiments:

- **Original Masks Experiment:**
  ![Original Masks](https://github.com/Mreeb/Segmentation-using-Point-Annotation_or_incomplete_tagging_UNet/assets/103059817/f34920b2-b813-4eda-ac2a-00868b658150)

- **Point Masks Experiment:**
  ![Point Masks](https://github.com/Mreeb/Segmentation-using-Point-Annotation_or_incomplete_tagging_UNet/assets/103059817/e7392c69-bb9b-4816-8133-c19ff8bbe38e)

Thank you for exploring these insights with me.
