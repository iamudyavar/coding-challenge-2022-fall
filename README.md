# Predicting Car Prices

## The Problem

Pricing a car competitively is a tricky problem for car sellers. The price cannot be too high as the car won't sell, but the price cannot be too low since the seller would make a loss.

I set out to solve this problem by creating a program which can predict the price of a car based on some of its features.

## My Approach

The first thing I did was analyze the dataset provided to see what features I could use. I was looking for qualities of the car that would correlate the most with price. To visualize the data using Python, I used the ```seaborn``` library and created a pair plot.

After analyzing the scatter plot of all the data points graphed against each other, I noticed that the ```Year```, ```Mileage```, and ```Used/New``` columns had a large factor in determining the price. There was a clear exponential correlation between price and year / mileage. Furthermore, although there were no "New" cars in the dataset, it appeared that "Certified" cars were newer and had less miles on them.


![](https://i.vgy.me/fZjP7n.jpg)

---

## Creating the program

To work with the dataset and train a ML model, I used Python along with the ```pandas``` library and the ```scikit-learn``` library respectively. Now that I had figured out what data points I would be using, I cleaned up the ```Price``` column and turned it into an integer, while also encoding the ```Used/New``` column so that it could be used in the ML algorithm.

Before continuing, I started to explore which ML algorithm was appropriate for this problem. Since ```Price``` was a continous value, I used a decision tree regression algorithm to predict the price based on year, mileage, and used/new status.

After splitting the dataset into training and testing, I created a new ```DecisionTreeRegressor()``` and trained the model. The model was a great fit, having a $r^2$ score of around -0.7. I also allowed for user input to let a seller input the features of their car into the model and get the predicted price.

## Conclusion

Through this coding challenge, I learned the nuances of Python and also why it is extremely powerful for ML. It was truly a learning experience for me to combine my statistics and programming knowledge to solve a real-world problem. I also got to know the libraries of Python much better as well as how to tackle a database with a large number of datapoints.

---

## Resources

[Seaborn API](https://seaborn.pydata.org/api.html)

[Scikit-learn API](https://scikit-learn.org/stable/modules/classes.html)

[Pandas API](https://pandas.pydata.org/docs/reference/index.html)

[Types of ML Algorithms](https://www.sas.com/en_gb/insights/articles/analytics/machine-learning-algorithms.html#)

[Python Docs](https://docs.python.org/3/tutorial/)
