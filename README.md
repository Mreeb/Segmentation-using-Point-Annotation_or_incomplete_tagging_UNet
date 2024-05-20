
#Exploring Factors Affecting Remote Sensing Image Segmentation using few points instead of full masks.

Introduction:
In this assessment, I delved into the challenges of segmenting remote sensing images, focusing on the impact of two factors: point annotation density and contrast enhancement. The goal was to understand how these factors influence the accuracy of segmentation models in identifying water bodies.

Methodology:
To start, I used a UNet architecture for segmentation, tweaking it with custom encoder and decoder blocks. The model was trained using the Adam optimizer with a learning rate of 0.001 and binary cross-entropy loss. My investigation centered on:

Point Annotation Density: I experimented with different densities of point annotations, ranging from 50 to 200 points per image.
Contrast Enhancement: I explored the effect of contrast enhancement techniques on segmentation accuracy by preprocessing input images.

Experimental Process:

Purpose/Hypothesis:

Point Annotation Density: I suspected that more points would give the model a better grasp of the spatial layout, potentially improving accuracy.
Contrast Enhancement: I believed enhancing contrast could help the model better distinguish between water bodies and surrounding features.

Experiment 1: Point Annotation Density

Process: I generated point labels from full segmentation masks and varied the number of points per image.
Results: Training the model with different densities of point annotations revealed a positive relationship between point density and segmentation accuracy. More points meant better results.

Experiment 2: Contrast Enhancement

Process: I tried out contrast enhancement techniques like histogram equalization on input images.

Results: Using contrast-enhanced images, the model showed improved accuracy compared to the baseline. Enhanced contrast helped the model better discern water bodies, leading to sharper segmentation.

Conclusion:
In wrapping up, I found that both point annotation density and contrast enhancement play crucial roles in remote sensing image segmentation. More points mean better accuracy, and enhancing contrast can significantly improve the model's ability to distinguish features. These insights are vital for optimizing segmentation models for real-world applications.

Future Directions:
Moving forward, I plan to explore additional factors influencing segmentation performance, such as the distribution of point annotations and the integration of advanced data augmentation techniques. Additionally, I aim to test the robustness of these techniques across different environmental conditions and datasets for more comprehensive insights.


I also Experimented with the original masks of the dataset here are the results
![image](https://github.com/Mreeb/Segmentation-using-Point-Annotation_or_incomplete_tagging_UNet/assets/103059817/f34920b2-b813-4eda-ac2a-00868b658150)


And these are the Results from the Point masks.
![image](https://github.com/Mreeb/Segmentation-using-Point-Annotation_or_incomplete_tagging_UNet/assets/103059817/e7392c69-bb9b-4816-8133-c19ff8bbe38e)

