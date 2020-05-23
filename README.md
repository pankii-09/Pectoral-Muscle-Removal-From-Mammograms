# Pectoral Muscle Removal from Mammograms
<figure>
  <img src="https://github.com/gsunit/Pectoral-Muscle-Removal-From-Mammograms/blob/master/assets/processing-screenshot.png" alt="algorithm-screenshot"/>
</figure>

Pectoral segmentation is important as the pectoral muscle region and the breast region may have similar intensity or texture appearance.

Both the the tumor cells and pectoral muscle region tend to be brighter (more dense) than the breast region in the mammogram.

Thus, including the pectoral muscle region into breast density quantification may lead to inaccurate breast density estimation.

Source: https://www.sciencedirect.com/science/article/pii/S1361841518301129

## Glossary
### Mammograms
A mammogram is an X-ray picture of the breast. Doctors use a mammogram to look for early signs of breast cancer. The one shown above is called a mediolateral mammogram.

### Pectoral muscle
Pectoral muscles (colloquially referred to as "pecs") are the muscles that connect the front of the human chest with the bones of the upper arm and shoulder. 

### Canny edge detection
Canny Edge Detection is a popular edge detection algorithm. Using Canny Edge Detector solely for pectoral muscle segmentation produces quite unsatisfactory results. Thus, we use hough transform line detection.

### Hough Transfrom
The Hough transform is a technique which can be used to isolate features of a particular shape within an image. Because it requires that the desired features be specified in some parametric form, the classical Hough transform is most commonly used for the detection of regular curves such as lines, circles, ellipses, etc.

## Algorithm
<img src="https://github.com/gsunit/Pectoral-Muscle-Removal-From-Mammograms/blob/master/assets/algorithm-flowchart.png" alt="algorithm-screenshot" height="900"/>

## Scope for improvement
- The algorithm seems to produce satisfactory result on the images. However, not so much on the last image, `mammo_5.jpg`. This is so because the pectoral region here can not simply be modelled by a single line.
- We can repeatedly apply this algorithm on such images, and try to chisel away remaining parts of the pectoral muscle in each iteration.
- The parameters for the shortlisting lines have been chosen manually. However, they can be easily learned given a bigger dataset.

> Give me a place to stand, and I shall move the earth. - Archimedes

> Give me more data, and I shall learn the parameters. - Me :)


### Please refer `pectoral-segmentation.ipynb` for the complete code. I have tried to explain each step as clearly as I could.

### PRs welcome. ❤️😃
