# Zillow Regression Project

#### View my final powerpoint by clicking the link below
- [Zillow-Project-Slideshow](https://www.canva.com/design/DAEhUSbRcyM/4YXSwC3HlhsAWvHlPb94xg/view?utm_content=DAEhUSbRcyM&utm_campaign=designshare&utm_medium=link&utm_source=publishsharelink).

#### Project Objectives
> - you will need to reference the properties_2017 and predictions_2017 tables.
> - For the first iteration of your model, use only square feet of the home, number of bedrooms, and number of bathrooms to estimate the property's assessed value, taxvaluedollarcnt. You can expand this to other fields after you have completed an mvp (minimally viable product).
> - You will need to figure out which field gives you the annual tax amount for the property in order to calculate the tax rate. Using the property's assessed value (taxvaluedollarcnt) and the amount they pay each year (<field name>) to compute tax rate.
> - You will want to do some data validation or QA (quality assurance) to be sure the data you gather is what you think it is.
> - You will want to make sure you are using the best fields to represent square feet of home, number of bedrooms, and number of bathrooms. "Best" meaning the most accurate and available information. Here you will need to do some data investigation in the database and use your domain expertise to make some judgement calls.

### Project Planning 

The following link contains my project planning process on my Trello Board: https://trello.com/b/72W3Coxt/zillowregresssionproject

Here is a snapshot of my project planning from my Trello Board

![image](https://user-images.githubusercontent.com/80718476/122064596-e2569880-cdb6-11eb-805f-7bc4c891acf9.png)

### Project Summary
<hr style="border-top: 10px groove blueviolet; margin-top: 1px; margin-bottom: 1px"></hr>


#### Audience
> - Zillow Data Science team

#### Project Deliverables
> - A report in the form of a presentation, verbal supported by slides.

> - The report/presentation slides should summarize your findings about the drivers of the single unit property values. This will come from the analysis you do during the exploration phase of the pipeline. In the report, you should have visualizations that support your main points.

> - A github repository containing your work.

   > - This repository should contain one clearly labeled final Jupyter Notebook that walks through the pipeline, but, if you wish, you may split your work among 2 notebooks, one for exploration and one for modeling. In exploration, you should perform your analysis including the use of at least two statistical tests along with visualizations documenting hypotheses and takeaways. In modeling, you should establish a baseline that you attempt to beat with various algorithms and/or hyperparameters. Evaluate your model by computing the metrics and comparing.

   > - Make sure your notebook answers all the questions posed in the email from the Zillow data science team.

  > - The repository should also contain the .py files necessary to reproduce your work, and your work must be reproducible by someone with their own env.py file.
  
  > - As with every project you do, you should have an excellent README.md file documenting your project planning with instructions on how someone could clone and reproduce your project on their own machine. Include at least your goals for the project, a data dictionary, and key findings and takeaways. Your code should be well documented.


#### Data Dictionary
    
- This is a data dictionary as a reference for the variables used within in the data set.
 |   Target    |  Data Type   | Description    |
| :------------- | :----------: | -----------: |
|  taxvaluedollarcnt | float64   | The total tax assessed value of the parcel |

|   Feature      |  Data Type   | Description    |
| :------------- | :----------: | -----------: |
|  bathroomcnt | float64   | number of bathrooms  |
| bedroomcnt   | float64 | number of bedrooms|
| calculatedfinishedsquarefeet   | float64 | Calculated total finished living area of the home |
| propertylandusetypeid  | float64   | Type of land use the property is zoned for|
| taxamount  | float64 |The total property tax assessed for that assessment year|
| yearbuilt  | float64 |  The Year the principal residence was built |
| fips  | float64 | Federal Information Processing Standard code -  see https://en.wikipedia.org/wiki/FIPS_county_code for more details|
| parcelid | float64 | Unique identifier for parcels (lots) |



#### Initial Hypotheses

> - **Hypothesis 1 -** I rejected the Null Hypothesis; there is a relationship.
> - alpha = .05
> - $H_0$: Square feet has no relationship on tax value dollar count. 
> - $H_a$: Square feet has a relationship on tax value dollar count. 

> - **Hypothesis 2 -** I rejected the Null Hypothesis; there is a difference and this did not happen by chance.
> - alpha = .05
> - $H_0$: There is no difference between bedroom count and tax value dollar count.
> - $H_a$: There is a difference between bedroom count and tax value dollar count.

> - **Hypothesis 3 -** I rejected the Null Hypothesis; there is a difference and this did not happen by chance.
> - alpha = .05
> - $H_0$: There is no difference between bathroom count and tax value dollar count.
> - $H_a$: There is a difference between bathroom count and tax value dollar count.

<hr style="border-top: 10px groove blueviolet; margin-top: 1px; margin-bottom: 1px"></hr>

### Executive Summary - Conclusions & Next Steps
<hr style="border-top: 10px groove blueviolet; margin-top: 1px; margin-bottom: 1px"></hr>
<b>The following are key takeways:</b>

  -There is not one main driver for tax value.
 
 - Logistic regression is better than baseline but with more time I would continue to work with this model to improve the accuracy score
  
  - The models I created were a  Linear Regression, Lasso Lars, and Tweedie Regressor. All of the models outperformed the baseline. I chose was the linear regression as my best model with a 10 % improvement for predicting features of Tax Value: Caculated Finished Square Feet, bedroom count, and bathroom count.
  
  -  The linear regression  outperformed my baseline score by 10 % thus it has value.


<hr style="border-top: 10px groove blueviolet; margin-top: 1px; margin-bottom: 1px"></hr>

### Pipeline Stages Breakdown

<hr style="border-top: 10px groove blueviolet; margin-top: 1px; margin-bottom: 1px"></hr>

- Acquire the data
- Prepare and clean data
- Explore 
- Model & Evaluate
- Recommendataions


___

<hr style="border-top: 10px groove blueviolet; margin-top: 1px; margin-bottom: 1px"></hr>



### Reproduce My Project

<hr style="border-top: 10px groove blueviolet; margin-top: 1px; margin-bottom: 1px"></hr>

You will need your own env file with database credentials along with all the necessary files listed below to run my final project notebook. 
- [x] Read this README.md
- [ ] Download the aquire.py, prepare.py, and zillow_final.ipynb files into your working directory
- [ ] Add your own env file to your directory. (user, password, host)
- [ ] Run the zillow_final.ipynb notebook
