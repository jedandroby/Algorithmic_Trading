# Algorithmic_Trading
Challenge 14 for Fintech bootcamp through UC Berkeley. Using machine learning to create simple trading algorithms and back test the model and optimize/tune it for better performance.


- changing length of training
Training the model on different lengths of time (everything from 3months to 12 months)i was getting an error every time i tried to set the training period to something longer than 12 months. Did not seem to change the quality of the model, the `classification_report` did tune a little with different lenghts, but nothing significant that seemed to show a pattern. The main change was the results of the actual returns, due to a different starting point for the testing period. This would mean that the 'entry' point for the investment happened at a different price resulting in different returns. Model performance did not improve though.

- changing length of SMAs
best machine learning `classification_report` stats came from 21/150 SMAS, WITH PRECISIONS having a value of .53 and .56 for -1 and 1 respectively. 
However, best results for investments off predictions came from 5/50 SMAs which did not have impressive results on the `classification_report` with precision results of 0.41 and 0.56 for -1 and 1 respectively. 
Changing the SMAs make a difference to the dataset, based on how long the SMAs are, this also results in changing the training data for the model, with different values to learn from when making predictions. The results could be noticed with some models performing signifcantly worse on the cumulative results compared to other models. Below is a screenshot of the model that seemed to perform the best, but is still very similar to the base strategy. 

the most successful strategy using the svm model turned out to be the 5/50 sma combo and flipping the strategy with 1 and -1. 