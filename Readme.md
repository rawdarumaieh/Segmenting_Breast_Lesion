# <p style="text-align: center;"> Advanced Topics in Image Processing Final project </p>
### Team Members:
1. Ahmed Mahmoud Fawzi &rarr; 1170523
2. Amira Ahmed Nouman &rarr; 1170400
3. Rawda Ahmed Rumaieh &rarr; 1170448

### Submitted to:
#### Dr. Ibrahim Sadek
#### <p style="text-align: center;">  ----------------------------------------------------------------------------------------------- </p>

#### To run the code:
1. **Put the data in the directory including Jupyter notebook**
2. **In the data file make sure to have two folders one called GT and the other is called input**
#
### Functions Implemented:
#### **invert** &rarr;     Function responsible to invert black and white colors

#### **lee_filter** &rarr;  Filter to decrease speckle noise 

#### **PlotAnnotations_General** &rarr;         Function responsible to plot the Segmented Output along with the FN(red color) and FP(green color) *Inputs: Ground Truth Image Segmented Image*
#### *Outputs:Colored Image showing  Segmented Output,FN,and FP*
#### **PlotSaveImage** &rarr;      Function responsible to clear any extra region attahced to the border of the image
#### **IMclear_Border** &rarr;     Function responsible to clear any extra region attahced to the border of the image

#### **GetMaxAreaRegion** &rarr;  Function responsible to calculate the max area region and clear others
#
### Code Explanation:
1. Intializing the variables we will use in statistical analysis 
2. Creating and Clearing the Results folder to add new images
3. Main Loop [Pre-processing, Segmentation and Post-Processing for each image]
   * Start Timer
   * Split the name and extension for the image 
   * Contrast Stretching
   * Image Invertion
   * Applying lee-Filter to Inverted Image
   * Image Enhancement (Egde Enchancement Mainly)
   * Normalizing Image
   * Apply Slic Segmentation which *segments image using k-means clustering in Color-(x,y,z) space*
   * Coloring the Segements
   * Thresholding
   * Clearing border (*removing regions sticking to border*)
   * Getting the region with maximum area (*lesion*)
   * Statistics 
   * Plot Annotations
   *Stop the timer 
4.Creating the statistics table
5.Saving the table as excel file 
