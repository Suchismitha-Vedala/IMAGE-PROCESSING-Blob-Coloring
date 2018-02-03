
Resize

Given an image , we binaries the image, i.e make it a array of 0s and 255s.

a.	Compute Histogram:
Read the image as gray scale image. For each pixel value, we increment the hist array with the counts of the intensity values of the image. This is then plotted using matplot.




Optimal Threshold:
Optimal threshold is calculated as follows:
1.Find the initial mean from the histogram.
2. Find the average of the expected values from 0 to initial mean.
3. Find the average of the expected values from initial mean to end.
4. optimal threshold is the mean of the two.
Repeat steps 2-4 until the threshold becomes constant. We return that value as our optimal threshold.


b.	Blob coloring:
Since the given output image has a reverse visualization of binary(white and black), we first inverse the given binary image ,i.e making 0?s 255 and 255?s 0. In our image, we need to find all those regions which are different, i.e the white spots. Therefore we check for only those pixels whose value is not 0. We perform blob coloring algrorithm and assign region numbers to each pixels. All pixels with similar number fall into one region. We return the region, list of all the pixels with that region number.

c.	Cell Counting:
The area of the regions is the number of pixels present in the region, i.e 10 pixels in a region: area=10
The centroid of regions is found by taking all the x and y coordinates in lists, 
X_centroid=sum(x_list)/length(x_list)
Y_centroid=sum(y_list)/length(y_list)

Region Mark:
We now mark the centroid points on the image using  opencv and also mark the area, region number along it. 






