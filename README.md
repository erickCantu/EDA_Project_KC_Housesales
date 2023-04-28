# Exploratory data analysis on the House sales in the King County dataset. 

At the Neuefische bootcamp, the EDA work was performed to the House sales in the King County dataset. The dataset is publicly available at [Kaggle](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction). To simulate a world case scenario. Different stakeholders with individual requirements were previous established by the Neuefische team. In this analysis I simulated a realtor company who conducted the EDA to fulfill the needs of a fictional investor named Timothy Stevens. Mr Stevens sells houses and is interested in putting his investments in the market. He owns expensive houses in the county center, which are the analysis target. The best timing for him is within a year. He is open for renovation if profits rise with it. 

---
The analysis

At Red Cedar Property Advisors (RCPA) we specialize in providing the best advice to buy or sell your real state properties. We cover the King County in Washington State.

Our customer Timothy Stevens asked for our advice. He is interested in selling some of his properties in the center of the County within the next year. A key question that he brought to us was: Is it worth it to renovate the properties? Although he is opened in doing it, it will only be done if there is a profit benefit.

---

#### Main results:

The mean prices per zip code in the King County are quite disperse. The price range goes between 2.4 and 11 million. Because of this disperse, through the analysis I identified that anything bigger than 4 million is assumed its an outlier.

Unfortunately, our customer the properties in the county's center are not reflected in these prices. **Note to the reader:** *In the assessment description, I did not had information on the exact location of the stakeholder properties. Because of that, I use the city of Seattle as the base for the analysis*

#### Is it worth to remodel?

Quite understandable the property and construction size correlate with the price. The bigger the property and its construction, the higher the market price. In our analysis we discover other factors that also have a slight correlation with the price in the center of the county . Current house condition and house grade (~0.63).  
![image](/images/houses_seattle_75_corr.png)
The house condition relates to the maintenance stage of the house, e.g. if it requires repair or how much work on it is required. While house grade relates on how good its construction meets the building code. From not meeting it, to a custom design.

In our analysis we found that improving the house condition or grade do not had an impact in the price. This result is only valid for the center of the city of Seattle and do not represent the whole County. Therefore RCPA gave the recommendation: do not remodel. Sell as is.

![image](/images/houses_seattle_condition_mean_price.png)

#### Takeaways

- The minimum price to sell is $ 675,000.
  
- House Condition and Grade drive the price.
  
- Do not remodel, it is not profitable in the city of Seattle.

---
#### Files
- [Jupyter Notebook](2022-06-01_eda_project.ipynb) 
- [Presentation](eda_Seattle_City_Center_Housing_Market.pdf) 
---
## Requirements

- pyenv
- python==3.9.8

## Setup

One of the first steps when starting any data science project is to create a virtual environment. For this project you have to create this environment from scratch yourself. However, you should be already familiar with the commands you will need to do so. The general workflow consists of... 

* setting the python version locally to 3.9.8
* creating a virtual environment using the `venv` module
* activating your newly created environment 
* upgrading `pip` (This step is not absolutely necessary, but will save you trouble when installing some packages.)
* installing the required packages via `pip`

At the end, you want to make sure that people who are interested in your project can create an identical environment on their own computer in order to be able to run your code without running into errors. Therefore you can create a `requirements file` and add it to your repository. You can create such a file by running the following command: 

```bash
pip freeze > requirements.txt
```

*Note: In rare case such a requirements file created with `pip freeze` might not ensure that another (especially M1 chip) user can install and execute it properly. This can happen if libraries need to be compiled (e.g. SciPy). Then it also depends on environment variables and the actual system libraries.*

### Unit testing (Optional)

If you write python scripts for your data processing methods, you can also write unit tests. In order to run the tests execute in terminal:

```bash
pytest
```

This command will execute all the functions in your project that start with the word **test**.
