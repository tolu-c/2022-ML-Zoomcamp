# Week 01

- [Week 01](#week-01)
  - [Notes](#notes)
    - [1.1](#11)
    - [1.2 ML vs Rule-Based Systems](#12-ml-vs-rule-based-systems)
    - [1.3 Supervised ML](#13-supervised-ml)
    - [1.4 CRISP-DM ML Process](#14-crisp-dm-ml-process)
      - [Steps](#steps)
    - [1.5 Modelling Step: Model Selection](#15-modelling-step-model-selection)
      - [Selecting the best model](#selecting-the-best-model)
      - [Multiple comparisons problem](#multiple-comparisons-problem)

## Notes

### 1.1

ML is a process of extracting patterns from data.
data can be of two types:

- features: information about the object
- target: what we wanna predict about the object

The resulting pattern is called **model**

> Features + Model = Predictions

### 1.2 ML vs Rule-Based Systems

Solving the spam detection using ML:

- Get data
- define and calculate the features(rules or what identifies as spam)
- train and use the model

> Binary features are features that can only take two values

rule based
> data + code -> software -> outcome(spam/good)

ML
> outcome(spam/good) + data(emails) -> ML -> model
> hence data + model=> outcome(spam/good)

### 1.3 Supervised ML

teaching ML by showing examples
Examples:

- regression => outputs a number
- classification => output a category
  - Multi-class => outputs subcategories of the a category
  - Binary => outputs only two values
- Ranking => outputs a rank(chooses something over another)

### 1.4 CRISP-DM ML Process

CRISP-DM -> Cross Industries Standard Processing Data Mining.
It's a methodology for organizing ML projects

- understand the problem
- collect the data
- train the model
- use it

#### Steps

1. **Business understanding**: identify the business problem, understand how we can solve it.
   > Ask yourself, "Do you actually need ML?".
2. **Data understanding**: identify and analyze the available data sources, decide if you are gonna need more data.
3. **Data preparation**: transform the data so it can be put into the ML algorithm.
   - Clean the data
   - Build the pipelines(sequence of steps)
   - Convert to tabular form
4. **Modelling**: train the model
   Training a model involves:
   - trying different models
   - selecting the best one
5. **Evaluation**: measure how well the model performs according to goals set in step 1.
   > *Was the goal achievable?*
   > *Did we solve/measure the right thing?*
6. **Evaluation + Deployment**: online evaluation(live testing)

### 1.5 Modelling Step: Model Selection

Models to choose from:

- Logistic Regression
- Decision Tree
- Neural Network
- or many others

#### Selecting the best model

you divide your data set into two:

- Train data (about 8% of the data) *y1*
- Validated data (about 20% of the data, presumed data of the future) *y2*

train both and compare
> repeat for the other models, compare and select the best model

#### Multiple comparisons problem

> A model might be **lucky** but not **accurate**.

How to avoid that? split the data into three:

- Train data
- validation data
- test data

> hence, perform multiple data validation to avoid being lucky.
>
> SPLIT => TRAIN => VALIDATE => SELECT => TEST => CHECK
