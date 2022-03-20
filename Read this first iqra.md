**Please go through the thesis pdf. I have highlighted some part and annoted within the document.You might have to download the pdf to see the annotations**

**Read this after**
## General Observations:
- we didnt give enough importance to differentiate dialect vs accent... both are not same...
  An accent is simply how one pronounces words—a style of pronunciation. A dialect includes not just pronunciations, but also one’s general vocabulary and grammar.
- Research problem statement need to be much more precise! 
- In features description part, the figures we have shown arent adding much to the research. I get it they are good for showing what the features are. **Instead**, we can show summary stats,,,
for example; for amplitude envelope we can find the mean value of each of the regions and plot them to show the difference. This can be done for:
  - AE
  - ZCR
  - RMSE
  - Spectral Centroid
  - Spectral Bandwidth
- Did you use Kfold/stratifiedkfold for validation of the dataset? The writing *Train,Validation and Test split* isnt clear enough. From my understanding it seems a basic implementation. Its hard to get **correct** accuracy in this manner since this accuracy has overly optimistic bias towards the model. As a result its not representation of how well the model generalizes. 
- In Training parameter part, we can do much more. Basically we just handpicked hyperparameter values and checked which one works. Although, this is the correct approach most of the time. Theres three ways to go when searching in hyperparameter space:
  - Exhaustive Search / GridSearch
  - Randomized (works best)
  - Bayesian Optimization (Time consuming)
I have worked with the first two on sklearn and with Cross Validation they are around 10 to 15 lines of code! I just checked Keras documentation and they also have built in module for implementing these! I think we can do this!
- NO validation curve of learning curve were given! I think we can proove with the learning curve, if we had more data the accuracy of our model would certainly increase! We can plot these two! 
