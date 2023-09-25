# ds-project-template

Template for creating ds simple projects

## Requirements

- pyenv
- python==3.11.3

## Setup

One of the first steps when starting any data science project is to create a virtual environment. For this project you have to create this environment from scratch yourself. However, you should be already familiar with the commands you will need to do so. The general workflow consists of... 

* setting the python version locally to 3.11.3
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


### Environment

This repo contains a requirements.txt file with a list of all the packages and dependencies you will need. Before you install the virtual environment, make sure to install postgresql if you haven't done it before.

```bash
brew update
brew install postgresql
```

In order to install the environment you can use the following commands:

```
pyenv local 3.11.3
python3 -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
pip install geopandas
pip install folium
pip install geopy
```


### Spiced Academy / Data Science Bootcamp / Week 03 / 1. Test "EDA Exercise"

1. I used the provided template.

2. I filtered and downloaded King County housing market data with SQL queries from online database via web access.

3. I explored randomly at first and plotted some graphs freestyle.

4. I developed multiple hypothesis and run the prospective plots to confirm or disprove my estimates.

5. I additionally went to  official King County Sheriff's website and downloaded crime statistics to improve my recommendation for my client because due to her name (Nicole Johnson) and location (KC, USA) an LLM estimated her to be most probably a 30-something business lady.

6. I exported all to my search (Lively, central neighborhood, middle price range, right timing (within a year) relevant plots for building my presentation.

7. I also exported the top 10 homes to use in Excel and Powerpoint as LowCrimeCityCenter.csv.

8. I exported my top 3 recommendations for my client as interactive HTML map (Top_3_Locations_Map.html).

9. I created an intro mood video showing a day in the life of my client living in King County and Seattle.

10. I cerated a 2nd video a screen recording of me using my HTML map to use in my presentation.

11. I fine-tuned presentation, typo, visuals, plots, etc. – and pushed everything back to Repo.


