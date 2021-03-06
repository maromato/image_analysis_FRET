# image_analysis_FRET

This is the code for data visualization and analysis for images with FRET based flourecent probe called SCAT3.2 for surviving and apoptosis cell distinction.
Suviving cells have FRET signal and apoptotic cell have Amcyan signal. Nomalized FRET signal (FRET/Amcyan) value (intensity) indicate cell viability.

### 1. dataset
Sample data.zip file contains 10 visal fileds data from two non-treated mice and 10 visal fileds data from two chemotherapy treated mice (5 visual fields from individual mice). The data are text files for nomalized FRET signal for individual 512 X 512 pixel areas.

### 2. initial image analysis for ratiometry with Image J/Fiji

The original image was processed by Image J function.
The detail was described elsewhere (https://imagej.net/Image_Intensity_Processing)

1. ROI is selected.
2. Ratio of FRET(channel 2) and Amcyan (channel 1) is calculated by "Image Calculator function..." (under the menu of process) after background correction.  
3. the result of Image calculation is saved as "Text Image..."

### 3. further image analysis with R

The code called "SCAT3_2_analysis.R" for further image analysis.

It contains code

1. To make a heatmap of imaged area
2. To make histgram plot of normalized FRET (F/A) value
3. To make summary bar chart and conduct statistical analysis (t-test)
4. To make a heatmap for entire dataset

<img width="1004" alt="Screen Shot 2020-10-14 at 12 58 12 AM" src="https://user-images.githubusercontent.com/17135389/95948918-89fe6f80-0dbf-11eb-9bea-8830223689f2.png">

### 4. Software and miscellaneous

The programs were written by R 3.6.1.
This is a beta-test version for educational/research purposes and please let me know if there are any questions.

email: toshihiko.oki@gmail.com

