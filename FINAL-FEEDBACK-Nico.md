### ***Final Project Feedback***

***Nico Van de Bovenkamp***

***

**Overall**  
Great work on this final project! You picked a challenging, yet reasonable project that was perfect for this class. I hope you enjoyed it, and I hope you learned a lot! You did a ton of data cleaning, and in some fairly efficient code (apply functions are perfect, as they are array operations and, thus, parallelized operations). You also had some nice, written out logic for converting your data types and classification space. You also were very effective at interpreting your results, and used several of the techniques for investigating model coefficients and results seen in class. Below are some thoughts:

***Code***  
One of the major things you learn over time when developing is how to write effective, efficient code. There are a few spots where you could have increased the efficiency of your code (and readability). Making code more efficient will reduce debugging time, reduce code complexity and replication, and reduce time spent processing.

Another note is a few best practices. The first being writing functions and scripts in py files, which are then imported as your own modules and reused. This way you can use them again and again, without blowing up your exploration space. For example, you can script a ton of those plotting functions where you are doing the same task over and over. Also, I would suggest you write all of those transformations into classes/functions! This is especially important in production settings. Another best practice is to import all of your modules at the beginning of the files. If you find that you need something else, add to the top of the file.

***Features***  
Feature extraction is key in machine learning. As I said, models are important, but good data is much, much more important. With that said, you should try experimenting with extracting different feature sets. In this case, you could experiment with different uses of your TfIdf. You should play with the min document frequency parameter for sure! Also, you should certainly strip all integers (digits) from your text. They won't add much value, as your models indicate, but they do add complexity and reduce the impact of the features that do matter.

***Modeling***  
In your models, you went the route of several binary classification models over multi-class models. This is okay, but not really all that necessary. You could build a model where you use multi-class classification for logistic regression AND multinomialNB. As you noted, you are right that you cannot get an auc score for the multi-class case, but you can calculate that metric per class! You would just be doing three separate calculations. Also, on the note of model evaluation metrics, I recommend that you take a look at confusion matrices because they will give you solid insight into how your model was miss-classifying each class relative to the other classes!

Another note on modeling would be to make sure that you are optimizing your hyper parameters for each model. The base class is not optimized for your data, so you should tune those. In the case of NB it would be that alpha parameter. In logistic regression it is your L1 or l2 regularization (plus other things like your optimizer). Additionally, I believe this is why your random forest model was not so successful.

With all of those notes, there are some lessons on modeling. First, logistic regressions work very well for sparse data (like text data). They are implemented all over the place in areas where data is super sparse like in ad serving, and really any online setting where you have tons of features. I am surprised that random forests didn't work that well because they are fairly good at working in sparse (and dense) data with lots of features. The next big step would be Neural Networks like an LSTM (check it out)! Finally, linear regressions perform very poorly in sparse data. Text data like this adds far too much complexity to these models. What you could have done was add L1 regularization to dramatically reduce complexity (it is likely entirely necessary).

***Where to go from here***  
Now that you have made it through the course, I am sure you feel like you learned a lot, but have even more to learn. It's almost a bit overwhelming. As I said at the beginning of this course, the part-time course serves as a great base line for you to really start doing the work on your own, or out in the world. Now, what you do next is totally up to you, and totally dependent on where you want to take your skills given this experience. Maybe you want to practice coding and python for automating tasks or working with data. Maybe you want to just learn a bit more so that you have a better understanding of what the analysts, data scientists, and engineers do at work. But if you want to keep learning in this domain, then here are a few of my recommendations:  

* **Practice your programming and software development skills.**  One of the most important things to do as a baseline is just to get better at coding. Find a good book or series of online courses on python, whether it's for data science or just python in general, and dig in. From there, it's all about practice! Knowing some object-oriented programming, networking, working in a cloud environment, potentially some other languages/frameworks like tensorflow, pytorch, and scala, ssh, and other things will get you up to speed in this space.

* **Revisit the basics of statistics, machine learning, and deep learning.** Now that you have gone through all of these different models and approaches at a high level, you should spend some time going back to the basics. You should be able to answer questions like:   
    - what is a loss function?
    - what is supervised vs. unsupervised learning?
    - should you use a more "statistically oriented" model or machine learning model?
    - what are optimization techniques and how are they used?
    - what is the structure of this model?
    - what are common approaches for this problem?
    - what are common sampling techniques?
    - what is cross-validation?  

    Take a look at blogs like **KDNuggets** and various online Data Science community groups to find out what types of questions you should be able to answer!

* **Practice and read all the time!** Nothing beats experience, and there are tons of ways to get it. Go on kaggle and spend some time trying things out on datasets. Find a project at work, or with friends/a group, to work on. Surround yourself with people that are experienced (at work, I am around tons of people that are truly talented, and I learn tons from it!).

**I hope you enjoyed the course! If you have ever have any questions, don't hesitate to reach out via email (nico.vdb@nyu.edu or njvandebovenkamp@gmail.com)**  

**Best,  
Nico**
