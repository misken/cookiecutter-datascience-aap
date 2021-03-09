# Cookiecutter Data Science modified for our aap class

See [the Cookiecutter Data Science homepage](http://drivendata.github.io/cookiecutter-data-science/) for
all the details. As it says, this cookiecutter is:

_A logical, reasonably standardized, but flexible project structure for doing and sharing data science work._

I've simplified and revised things a bit for our class. As you become more proficient in using
various software engineering tools and figured out what works for you in terms of project structure,
 you can create your own customozed version of Cookiecutter Data Science.
 
Some of the big changes I made include:

* modified the folder structure to put a main package folder inside the `src/` folder,
* this modified folder structure necessitated some changes to `setup.py` to help it find the packages,
* ruthlessly removed as much as I could to keep things as simple as possible.


### Requirements to use this cookiecutter template:
-----------

I've already installed cookiecutter in our aap VM. So, the instructions below are only needed if you want
to either pip or conda install cookiecutter yourself on some machine or in some virtual environment.

 - Python 2.7 or 3.5+
 - [Cookiecutter Python package](http://cookiecutter.readthedocs.org/en/latest/installation.html) >= 1.4.0: This can be installed with pip by or conda depending on how you manage your Python packages:

``` bash
$ pip install cookiecutter
```

or

``` bash
$ conda config --add channels conda-forge
$ conda install cookiecutter
```


### To start a new project, run:
------------

    cookiecutter https://github.com/misken/cookiecutter-datascience-aap


### The resulting directory structure
------------

The directory structure of your new project looks like this. Of course,
you can always delete and add more folders as needed or desired. Leave the
src/ and main package subfolder of src/ alone unless you know what you
are doing (i.e. changes needed in setup.py).

```
├── LICENSE
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│
├── docs               <- A default Sphinx project; see sphinx-doc.org for details
│
├── models             <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── setup.py           <- makes project pip installable (pip install -e .) so {{cookiecutter.repo_name}} can be imported
├── src                <- Source code for use in this project.
│   ├── {{cookiecutter.repo_name}} <- Main package folder
│   │   └── __init__.py    <- Marks as package
│   │   └── {{cookiecutter.first_module_name}}.py  <- Just some placeholder Python source code file
│
└── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io
```

## Contributing

Hopefully, as the class goes on, we will all come up with ideas for improving this cookiecutter.
