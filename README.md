# analyticsproject
Data Analytics for Business project for an ITU Course. Project was about using finding a dataset and analysing it by using different machine learning algorithms on Python.


# Revision notes - 11.04.2022

After looking back at this project. I have seen some mistakes that were gone unnoticed by our graders and us project members.

First one I saw was a big mistake that I am sure a lot of amateur data scientists/analysts make which is scaling the data all at once. 
After a little research and experience it can be concluded that the test data should not in anyway be influencing the train data.
Scaling is influencing this massively by taking both the mean and standard deviation (we used StandardScaler from scikit-learn) of the train and test data combined.

Another mistake is a more general coding mistake which is not using functions. Since we were not very well coordinated for our project and none of us
had any collaborative programming experience, we did not use github or other platforms. We programmed seperately with the same train and test datasets. 
Not using functions and copy pasting the same lines of codes cause a small waste of time and an eye-bleach while reading the code. There are a lot of places that a function could be used. 
Especially KFold cross validation and feature selection methods (I remember using Forward Feature Selection).

Using confusion matrix was a good idea however we didn't know what it represented for multiclass target variable. We should've done some research on that
to see that we could still find the TP, FP, TN, FN values as well as recall and precision for each class. An easy mathematical formula can be seen below

![image](https://user-images.githubusercontent.com/86730879/162642445-453358b3-744a-4d31-8775-7ea92e355fa9.png)

**notes from stats.stackexchange :** ...Precision is the fraction of events where we correctly declared i out of all instances where the algorithm declared i. 
Conversely, recall is the fraction of events where we correctly declared i out of all of the cases where the true ~~of~~ state of the world is i.

There also has been an error which I will not try to find with the forward feature selection on logistic regression since the accuracy is suprisingly low compared to
other logistic regression models.


