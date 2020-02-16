## 1/23/20

### Data Prep Cheat Sheet

#### How did you decide to start writing down content?

We decided to first brainstorm the steps that we thought were required in order to properly prepare data.  Topics were vocalized extemporaneously as they were thought of.  This could be met with a nod or a further discussion of whether it was in the purview of what we were being asked.  If a conscientious was reached it was added to the board.

#### How did you decide to organize your content?

Once we had brainstormed all the steps we shifted the discussion to their correct order. We went in the order of start to finish debating each topic presented in its final place.  Once all of the topics were numbered we then proceeded to create our flowchart.

#### What pre-existing knowledge or expierences did you rely on?

Having worked on data that came to me in a hard to work with format.  I wanted to make sure that the list included saving in a useful file format.  Some data types are just immensely easier to work with than others.  I also brought up adding additional columns but after further discussion it was decided that didn't fall into the purview of preparing the data.

## 2/3/20  

### Lauren Cappiello

Applied Machine Learning Methods in Adjusting for Populations [differences]

"make sure we are all speaking the same language here"

Study ends up with generally worse conditions from the target population

??covariate data?? for target population
??parametric approach/methods??

??vector baseline covariate??

suppot - the people in our target population to be represented in study population not exact the same but we at least have all the individuals that we'd see

Covariates sufficent to account for the differences.

??nuisance functions??  -- something we have to esimate but they all join together to be useful so we don't really care what the parts are

imputation

weighting mean ratio and difference ratio and using it as a weight

propensity score -- your in a covariate group given your data

Binary regression

**Doubly Robust**
M and r need to be correctly estimated m a regrssion model r??

estimate nusiance functions using machine learning

assumptions for ML
root n consistency asytompic normality
??little o notation??

Donsker Condtion -- gives us guassian distribution

How does one chose the optimal machine learning approach

Super learning
* combine several candidate learners
* Invovles the use of cross-validation to select among many candidates
* the algorithms are weighted based on CV performance

Sample splitting like CV random roughly same sized subsamples

??trivariate standard normal distribution??

superlearner
 *GLM
 *GAM
 *rpart
 
 refresh on bootstrap
 
 **compared** 
 coverage propability goes along with each method
 parameteric
 ML
 ML w/ sample splitting --right on the money
 
 Sesnitivity analysis for the ignorability assumption whene arlier we said the covariate sufficent to explain the difference this covers when it's not
 
 ML applied to estimators mostly parametric
 
 causual inference


### Jane Guo

**Dimension reduction using linear regression**

Got a response function from the classification

Stacking -- collective decision strategy weighted penalty

## 2/3/20 

### Variable Selection

* Reflecting on the questions from class the biggest focus of interest was how many variables or what types of variables to use for analysis. These types of questions fell in line with the types our group asked. One trend of questions that differed from ours was around time. Particulary, how much time one should spend on variable selection. 

* We have learned some variable selection techniques in class so far. This includes subset regression and LASSO. Additionally, we have discussed confonders and moderators.  With these topics it has given me the idea that variable selection should be done methodically. Be adding and removing variables and checking the inter-relationship between the included variables we gain insight into potental solutions.

* I liked this discussion because we spoke more abstractly about variables what qualifies as one and how they can be used.  This is normally stuff that's taken for granted because your already have a data set in mind.

* The benefit of asking your own questions is in checking our understanding as well as exploring what interests us most about the topic.

* Variable selection is a huge component to analysis.  Without domain expertise it's really the only way to get an understand og the relationships at play. Data is so wide these days and variable selection is a key to any analysis.

## 2/10/20

###

* A commonality was the idea of assumptions.  When we learned linear models we learned the assumptions of using that model. Similar to what are group questioned was the idea of different models for different types of Y. With each new model comes new assumptions. Something that stood out as different from our questions were how to determine whether variables are affecting one another.

* In class we have moved on from linear regression to logistic regression. This shows there are different models for the different types of y we are examining. To me it seems we still you the underlying priciples of the linear model the only difference so far is "mapping" the y to a range that works for the type of y.

* In our group we spent a lot of time discussing real world uses for different types of y predictors and came up with some interesting use cases of when a non linear model would be needed.

* The types of thing we predict come in all shapes and sizes. I'm looking foward to moving into more new types of models that can be used for analysis. What we've learned can be used to explore other types of potential models.

## 2/14/20

### Write down everything you remember about logistic regression (No Notes)

We use logistic regression when we want to predict an outcome between two choices.  This is to say are $\hat{y}$ is true/false yes/no etc/etc.

We will still want to use continious variables as our $X_n$ but we must find a way to map values that can be from $-\inf$ to $\inf$ to ones that can only be from 0,1.  In this way our $\hat{y}$ is an odds ratio (propability).  We can think of this as the likelihood of are y=1 outcome to be true.  

When we take this form we can write things like *for ever 1mBar decrease in air pressure their is a 2 times for lieky to rain*.

This is using the logit function or the `log(odds ratio)` where odds ratio is $\frac{p}{1-p}$