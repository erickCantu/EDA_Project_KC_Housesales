# Exploratory data analysis on the House sales in the King County dataset. 

At the Neuefische bootcamp, the EDA work was performed to the House sales in the King County dataset. The dataset is publicly available at [Kaggle](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction). To simulate a world case scenario. Different stakeholders with individual requirements were previous established by the Neuefische team. In this analysis I simulated a realtor company who conducted the EDA to fulfill the needs of a fictional investor named Timothy Stevens. Mr Stevens sells houses and is interested in putting his investments in the market. He owns expensive houses in the county center, which are the analysis target. The best timing for him is within a year. He is open for renovation if profits rise with it. 



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
