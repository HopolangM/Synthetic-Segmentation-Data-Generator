# Synthetic segmentation training data generator

## Project description

- *Obtaining training data can be both challenging and costly. Particularly for specialised tasks like surface type segmentation, specific training datasets are often unavailable and necessitate manual labelling of images, a process that incurs significant expenses. Even when training data is available, it is typically insufficient in quantity for effective model training.*
- *Generative models offer a solution by enabling the creation of training data for targeted tasks. For instance, we could employ generative models to produce synthetic satellite images showcasing various surface types, complete with corresponding segmentation data.*
- The project is divided into two main components:
1. The first model focuses on generating satellite images depicting diverse surface types such as sand, roads, and mountains.
2. The second model is tasked with labelling the generated data into distinct classes corresponding to the different surface types.

## Deliverables
- *Provide a detailed list of all deliverables expected for this project. Ultimately the tasks that are planned for this project by the project team will be derived from this so be as clear and specific as possible.*
 ### Overall
- The core output of the project is a generative model capable of leveraging a small set of meticulously labelled training data to produce an unlimited quantity of synthetic training data along with corresponding labels.

 ### Data Science Specific
 -  Building the models (segmentation and image generation) for the project.
 ### Data Engineering Specific
 -  The project primarily leans towards Data Science, focusing on developing generative models and handling the labelling process. However, Data Engineering plays a crucial role in managing the data pipeline and ensuring the efficient flow of images into the models for 
    training.

 ### Contextual information
 - Provide whatever other information is available that can help contextualise the project scope and deliverables to the project team.
 - The project aims to generate a vast quantity of satellite images, which will serve as valuable training data for segmentation models or other downstream tasks.

  ## Team External links
  
- AWS S3 Bucket: arn:aws:s3:::2307-07-synthetic-segmentation-a
- Trello link: https://trello.com/invite/b/5btHedhq/ATTI48a0f001e868ec9c4bf50ccfdd368c5fA594B110/synthetic-segmentation-training-data-generator
- Discord Team name: 2307-07-synthetic-segmentation-training-data-generator-a
- Canva: https://www.canva.com/design/DAGBTMvFEok/4JNs9jQkc9o0KU3-OYb8pg/edit

## Team Members

- Maria Booysen 
- Desiree Malebana 
- Ninamukovhe Tshivhase 
- Nozipho Pretty Bhila 
- Joseph Mhlomi 
- Shedrack Efienokwu 
- Kala Prince Maponyane 
- Wycliffe Otieno 

## Environment

It's highly recommended to use a virtual environment for your project, there are many ways to do this,
below we have provided one example of how this can be achieved. Ensure when working on your project
to keep this section up-to-date so if anyone needs to run your code they know the exact steps needed
to get the appropriate environment ready. A person should be able to clone your repo and get up and
running with the instructions provided here.

### Setup - you only need to do this once

```bash
# make sure your pip in your base Python installation is up-to-date
python3 -m pip install -U pip
# install the virtualenv package
python3 -m pip install virtualenv
```

### Create the virtual environment - also typically only run when needed

```bash
# create a virtual environment in this directory called '.venv'
python3 -m venv .venv
# you should now see the folder `.venv` in your repo
```

### This is how you activate the virtual environment in a terminal and install the project dependencies

```bash
# activate the virtual environment
source .venv/bin/activate
# install the requirements for this project
pip install -r requirements.txt
```

## Tests

It's highly recommended to get in the habit of writing tests, especially once you've identified something
concrete that you can refactor into a reusable bit of code. This project has been seeded with a minimal
working example of a [refactored function](src/data/make_dataset.py),
[a notebook that can import this code](notebooks/0.0-example.ipynb) and
[a unit test to test the code behaves as expected](tests/test_make_dataset.py).

You can execute tests from the terminal by running `pytest`. IDEs like VSCode have built-in support for
executing and debugging tests through the "Testing" menu.

## Project Organisation

```ascii
├── LICENSE            <- Contains information about the legal terms and conditions under which
|                         the code can be used.
|
├── README.md          <- The top-level README for developers using this project.
│
├── docs               <- Use markdown. If/when the project becomes more complex consider migrating
|                         to something like pdoc or sphinx depending on the nature of the project.
|                         Think carefully about what documentation should sit alongside the code
|                         and what you can rather include in docstrings.
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering), and a
│                         short `-` delimited description, e.g. `1.0-initial-data-exploration`.
|                         Refactor the good parts. Don't write code to do the same task in multiple
|                         notebooks. If it's a data preprocessing task, put it in a file like
|                         `src/data/make_dataset.py`. If it's useful utility code, refactor it to
|                         `src` and import accordingly. Only commit clean notebooks (clear all cell outputs).
│
├── requirements.txt   <- The requirements file for reproducing the environment.
|
├── src                <- Source code. Refactor clean, re-usable code here.
│   │
│   ├── data           <- Separate your code base into logical groups, e.g. data, features, models, visualisation, etc.
│   │   └── make_dataset.py
│   └── ...
|
├── tests              <- Unit tests. Filename should start with "test_".
    └── test_make_dataset.py
```
