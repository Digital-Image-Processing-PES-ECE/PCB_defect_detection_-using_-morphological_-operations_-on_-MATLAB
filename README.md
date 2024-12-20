# PCB DEFECT DETECTION

### Project Description:
#### Summary - This project revolves around the detection of holes and open circuit by using morphological operations . The pre-processing steps involved converting it into grayscale,histogram equalisation,gaussian blur and binarization processes like thresholding was used. Opening and dilation was used and XOR operations were used for finding out the diffferences.Bounding boxes were later on applied to the defected areas.

#### Course concepts used - 
1. - Image Enhancement-histogram equalisation
2. -Thresholding and noise removal(gaussian and median filter)
3. -Morphological operations(Opening and dilating)
   
#### Additional concepts used -
1. -Xor operations for finding the difference
2. -Bounding box algorithm for defect detection
   
#### Dataset - 
https://www.kaggle.com/datasets/akhatova/pcb-defects/data

#### Novelty - 
1. -basic morpgological processes like dilating and opening did not involve complex segmentations

### steps-
1.Run the matlab code mentioned in the code.m file
2.Use the original image with no defects as the template and any of the test images mentioned.

### Outputs-
<img width="1118" alt="Screenshot 2024-11-17 at 12 22 34 PM" src="https://github.com/user-attachments/assets/58dd206d-03a9-48db-ac0d-6a0e627bd21e">

<img width="1138" alt="Screenshot 2024-11-17 at 12 23 20 PM" src="https://github.com/user-attachments/assets/d8276133-d77b-4f2a-9632-116fc0021448">
<img width="1117" alt="Screenshot 2024-11-17 at 12 24 09 PM" src="https://github.com/user-attachments/assets/a5f10623-328e-4cb9-9bea-34982068a2d8">

   
### Contributors:
1.RACHANA GB(PES1UG22EC225)

2.LIKITHA S (PES1UG22EC910)

### References:
1. -S. H. I. Putera, S. F. Dzafaruddin and M. Mohamad, "MATLAB based defect detection and classification of printed circuit board," 2012 Second International Conference on Digital Information and Communication Technology and it's Applications (DICTAP), Bangkok, Thailand, 2012, pp. 115-119, doi: 10.1109/DICTAP.2012.6215366.

2. -TY  - BOOK
AU  - Heriansyah, Rudi
AU  - Abu Bakar, Syed Ab Rahman
AU  - Zabidi, Muhammad
PY  - 2002/10/07
SP  - 
T1  - Segmentation of PCB Images into Simple Generic Patterns using Mathematical Morphology and Windowing Technique.

   
### Limitations and Future Work:
This works only on the template images used and its restricted to only open and missing hole detection.This can be exteneded to further defects of the PCB and can be made more accurate for other datasets by using machine learning.
