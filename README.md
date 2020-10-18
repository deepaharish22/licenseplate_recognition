# IMPORTING PACKAGES AND DISPLAYING IMAGE:
1. Importing necessary packages
       Opencv,Numpy,pytesseract\.
2. Path of pytesseract is mentioned using the pytesseract command\. 
3. Reading the image using opencv function imread () and displaying the same using imshow ()\.
4. Converting the image into greyscale using cv2.cvtcolor () by passing the image andcv2.COLOR_BGR2GRAY\.

#  LICENSE PLATE DETECTION:
5. To localize the license plate, a machine learning algorithm named  haarcascade which is pre-trained with several “positive” sample views of a particular object and arbitrary “negative” images of the same size is used\.
6. Using cascadeClassifier () function, we apply the algorithm to the region of the image and in turn it detects the object in question\.
7. With detectMultiScale the detected objects are returned as a list of rectangles\.
(Reference for Cascade classifier: \ https://sites.google.com/site/5kk73gpu2012/assignment/viola-jones-face-detection#TOC-Image-Pyramid) \.

8. Using for loop, bounding box is made for the license plate and the image is shown as well\.
 

# CHARACTER SEGMENTATION & RECOGNITION:
9. The image is cropped and it is converted into greyscale\.
10. Using threshold function we’re able to classify the pixel intensities in the greyscale image and create binary images \.
11.The text is extracted from the license plate using pytesseract function image
_to_string. where config is pgm(page segmentation mode)-11 which indicates that tesseract should only look for one line of text\.
(Reference: https://www.tutorialspoint.com/opencv/opencv_simple_threshold.html) \.
14. To place the boxes on characters of license plate I used the image_to_boxes function and stored it in the variable char_box\.

# LIST CREATION:
15. declaring a function Convert (string)\.
16. An empty list is created for the insertion of license plate characters\.
17. The string value gets stored in the list and it is returned and stored in variable named letters\.

# DETECTING CHARACTERS AND FEATURES:
18. Declaring two variables previous and count and initializing them to 0\.
19. To detect characters am using for loop so that it loops over char_box\.
20. Height and width of the cropped image is found out using shape () function \.
21. Using split () function, the characters are stored\.
22. Using if condition we have to check if 0th index of b is equal to letters [cnt]\.
23. Since everything is string I converted x, y, w, h into integer and rectangle is drawn using cv2. Rectangle () \.
24. Height, width and space is calculated and displayed. Count variable gets incremented by 1\.
25. Previous gets equal to width\.
26. Else continue \.
27. Finally detected license number is shown\.
