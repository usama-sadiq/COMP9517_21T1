# COMP9517  COMPUTER VISION  LAB-01  YEAR: 2021 TERM: 01

# AIM

# QUESTION 1  Contrast Stretching

## OBJECTIVE 

- Read a grey scale image (cat.jpg) and perform contrast stretching to improve the quality of the image.

## IMPLEMENTAION

- Read the image "cat.png".
- Convert the image from BRG to RGB.
- Find min and max pixel values in the RGB format image.
- Apply the following formula given in the Lab specification document.

![Alt text](./Contrast_Stretching_Formula.png "Contrast Stretching Formula")

- where 
    - Or = original image.
    - Tr = transformed image.
    - a = min pixel values allowed in an image (8-bit image, a = 0).
    - b = max pixel values allowed in an image (8-bit image, b = 255).
    - c min pixel values in a given image.
    - d max pixel values in a given image.

- Convert it back to 8 bit image.
- Convert the image from BGR to RGB.

## RESULTS

![Alt text](./question_1_result.png "Contrast Stretching Formula")