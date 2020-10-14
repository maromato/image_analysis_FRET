# image_analysis_FRET

This is the code for data visualization and analysis for images with FRET based flourecent probe called SCAT3.2 for surviving and apoptosis cell distinction.
Suviving cells have FRET signal and apoptotic cell have Amcyan signal. Nomalized FRET signal (FRET/Amcyan) value (intensity) indicate cell viability.

### dataset
The sample data sets contain 10 visal fileds data from two non-treated mice and 10 visal fileds data from two chemotherapy treated mice (5 visual fields from individual mice). The data are text files for nomalized FRET signal for individual 512 X 512 pixel areas.

### initial image analysis for ratiometry with Image J/Fiji

The original image was processed by Image J function.
The detail was described elsewhere (https://imagej.net/Image_Intensity_Processing)

1. ROI is selected.
2. Ratio of FRET(channel 2) and Amcyan (channel 1) is calculated by "Image Calculator function..." (under the menu of process) after background correction.  
3. the result of Image calculation is saved as "Text Image..."

### further image analysis with R

The code called "SCAT3_2_analysis.R" for further image analysis.

It contains code

1. To make a heatmap of imaged area
2. To make histgram plot of vormalized FRET (F/A) value
3. To make summary bar chart and conduct statistical analysis (t-test)
4. To make a heatmap for entire dataset
