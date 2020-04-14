# Odia-handwritten-Numeral-recognition
This article intend to show, how easily we can build a model for any indic character recognition

## Package used:
    OpenCV
    NumPy
    Matplotlib
    Seaborn
    ScikitLearn
## Data Set:
     Manually created in ms paint
     Size : 120 images of total 4 different numerals (417x293 pixels each): 
            30 sets of ‘୦’  in English it is 0
            30 sets of ‘୧’  in English it is 1
            30 sets of ‘୨’  in English it is 2
            30 sets of ‘୩’  in English it is 3
#### English Numerals corresponding to Odia Numerals
                English(0-9)              Odia(୦-୯)
                    0	                  ୦
                    1	                  ୧
                    2	                  ୨
                    3	                  ୩
                    4	                  ୪
                    5	                  ୫
                    6	                  ୬
                    7	                  ୭
                    8	                  ୮
                    9	                  ୯
# Steps to Follow:
    1.  Using openCV, convert the image to matrix, where each element of matrix represent the intensity  (in scale 0 indicate black region and 255 indicates white region) 
    2.  Keep the input in x(matrix representation of image)
        keep the label in y (1234 representing the 4 initial odia numeral ୦୧୨୩)
    3.  Make sure both x and y in numpy array format, else convert them accordingly
    4.  Reshape of x from ‘120 x 293 x 417’ to ‘120 x 122181’
    5.  Make the split of data
                train: 70%
                test:30%
    6.  Using ScikitLearn create any classification model
    7.  Train the model by train data
    8.  By using the trained model predict the label of test data
    9.  Accuracy is measured by comparing the predicted labels and actual labels of test data
                a.  Accuracy Score:xx%
                b.  Confusion Matrix
                c.  other accuracy measure
