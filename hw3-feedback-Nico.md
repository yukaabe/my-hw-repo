### ***Project 3 Feedback***

***Nico Van de Bovenkamp***

***

**Overall**  
Awesome work on this assignment! Not only did you build your models effectively and interpret your results well, but you ran an experiment with sklearn as well! This is a useful thing to experiment with, especially when you take advantage of the different things that sklearn has to offer: regularization techniques, other models, different optimization strategies, pre-processing functions, cross validation etc. What I recommend is that you take this analysis/model, and try your hand using sklearn! Maybe even try out some different types of models we have learned: KNN, Decision trees, random forest, boosted trees, naive bayes, or SVMs!

***On cross validations***  
The typical framework is to do a train, test split on your data. Then, *within* your training set, you build models and validate them. So, it is as though you have a mini test set (sometimes called a validation set). When you build your cross validations, you would ideally be cross validating on your training set, and then *later* you evaluate on the test set. Is this clear?

***Using some python basics***  
Don't forget to use some handy python basics! In the portion of your code where you are printing out the cross-val scores with different scoring metrics, try making it more 'pythonic' with the following:

```python
cv_scores  = dict()
scoring_methods = ['accuracy', 'precision', 'recall', 'roc_auc']
for method in scoring_methods:
    cv_scores[method] = cross_val_score(model, X,y, cv=5, scoring=method).mean()
    print(method, cv_scores[method])
```
