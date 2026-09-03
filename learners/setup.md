---
title: Setup
---

In this workshop, you’ll learn how to extract data from websites using Python — a process known as web scraping.

Episode 1 begins with an introduction to how websites are structured using HTML.
You’ll learn how to explore this structure using your browser and how to extract information from it using the `BeautifulSoup` package.

In Episode 2, you’ll learn how to retrieve the HTML of a webpage using the `requests` package and continue practicing how to parse and extract specific content with `BeautifulSoup`.

Toward the end of the workshop, in Episode 3, we’ll explore the difference between static and dynamic webpages, and how to scrape dynamic content using `Selenium`.

It is very important that the legal and ethical considerations accompanying any web scraping activity are considered. This is covered in detail by University of Birmingham library staff in the [Introduction to Web Scraping course](https://bham-carpentries.github.io/bham-introduction-to-webscraping/). For reference Episode 4 contains the material for the topic from that course but, due to time constraints, is not presented in the workshop.

This workshop is intended for learners who already have a basic understanding of Python. In particular, you should be comfortable with:

- Install and import packages and modules
- Use lists and dictionaries
- Use conditional statements (`if`, `else`, `elif`)
- Use `for` loops
- Calling functions, understanding parameters/arguments and return values

## Software Setup

### Python

[Python](https://python.org) is a popular language for research computing, and great for general-purpose programming as well.  Installing all of its research packages individually can be a bit difficult, so we recommend [Conda-forge](https://conda-forge.org/download), an all-in-one installer.

Regardless of how you choose to install it, **please make sure you install a Python version >= 3.9** (e.g. 3.11 is fine, 3.6 is not).

We will teach Python using the [Jupyter Notebook](https://jupyter.org), a programming environment that runs in a web browser (Jupyter Notebook will be installed by Miniforge). For this to work you will need a reasonably up-to-date browser. The current versions of the Chrome, Safari and Firefox browsers are all [supported](https://jupyter-notebook.readthedocs.io/en/stable/notebook.html#browser-compatibility) (some older browsers, including Internet Explorer version 9 and below, are not).

#### Steps:

1. If you already have Anaconda, Jupyter Lab or Jupyter Notebooks installed in your computer, skip to step 2. 

::::::::::::::::::::::::::::::::::::::::::::::: tab

### Lab PC

  a. Open [AppsAnywhere](https://apps.bham.ac.uk) from the Windows Desktop.
  b. Login to your University Microsoft account when prompted.
  c. Allow the browser to open the AppsAnywhere browser.
  d. In the search bar, search for "miniforge", which should bring up "Miniforge Python 24.3.0-0 with All school addons".
  e. Select "Launch" next to Miniforge or on its description page.
  f. When ready, launch Miniforge by pressing the Launch icor or double-clicking.
  g. This brings up a file folder, where you should double-click on "Miniforge Prompt".

### Other

a. Follow Miniforge's [download and installation](https://conda-forge.org/download/) and instructions for your respective operating system. If you are using a Windows machine, make sure you mark the option to "Add Miniforge3 to my PATH environment variable".
b. If you are using Mac or Linux, open the 'Terminal'. If you are using Windows, open the 'Command Prompt' or 'Miniforge Prompt'.

::::::::::::::::::::::::::::::::::::::::::::::::::::::


2. Activate the base conda environment by typing and running the code below to activate your environment.

```terminal
conda activate
```

3. Install the necessary packages by running:
```terminal
pip install requests beautifulsoup4 selenium webdriver-manager pandas tqdm jupyterlab
```

4. Start Jupyter Lab by running: 
```terminal
jupyter lab
```

5. In a new Jupyter Notebook run the following code in a cell to check the necessary libraries can be loaded:
```python
from bs4 import BeautifulSoup
import requests
from selenium import webdriver
from selenium.webdriver.common.by import By
import pandas as pd
```

## Data
The html used in Episode 1 and Jupyter notebooks containing the code content can be [downloaded](../episodes/data/PythonWebScrapingFiles.zip).
The Jupyter notebooks are intended for reference as ideally, you will create your own notebooks as you follow along during the course.

## Additional resources
- Mitchell, R. (Ryan E. ). (2024). Web scraping with Python : data extraction from the modern web (3rd edition.). O’Reilly Media, Inc.
- Chapagain, A. (2023). Hands-On Web Scraping with Python : Extract Quality Data from the Web Using Effective Python Techniques (Second edition.). Packt Publishing.
