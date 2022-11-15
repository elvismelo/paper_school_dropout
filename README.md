# On the Use of Explainable Artificial Intelligence to Evaluate School Dropout

Code for paper "On the Use of Explainable Artificial Intelligence to Evaluate School Dropout"

In the pipeline archive, let's take the following steps:

1. Load Libraries
2. Data Clean
3. Balance Data
4. Build a Black-Box Model
5. XAI Frameworks 

# Model Card

## Model Details
Elvis Melo created the model. A complete data pipeline was built using Google Colab, Scikit-Learn, Keras Tuning, TensorFlow to train a black-box model. The big-picture of the data pipeline is shown below:

<img src="https://github.com/elvismelo/paper_school_dropout/blob/main/flow_diagram.jpg" width=80% height=80%>

Here, yellow steps are related to data processing, green steps are related to decision making and xai, blue steps are related to the black-box model

## Intended Use

In this paper, we applying and evaluate XAI methods to predict students in school dropout situation, considering a database of students from the Federal Institute of Rio Grande do Norte (IFRN), a Brazilian technical school.

## Training Data

The database of the defined case study comes from the Federal Institute of Rio Grande do Norte (IFRN), which includes data information of students from all 19 Campi spread throughout the mesoregions of Rio Grande do Norte in Brazil. Information on the family, school performance, financial field, ethnicity, demographics, and work situation, are present in the dataset.

<img src="https://github.com/elvismelo/paper_school_dropout/blob/main/imbalanced_database.png" width=40% height=40%>

The dataset is available. to access it, simply send a request to the authors.

E-mails to request: elvis.melo.016@ufrn.edu.br, ivanovitch.silva@ufrn.br and danielgcosta@fe.up.pt

## Evaluation Data

The dataset under study is split into Train and Test during the build black-box model of the data pipeline. 80% of the clean data is used to Train and the remaining 20% to Test. Additionally, 20% of the Train data is used for validation purposes (hyperparameter-tuning).

## Metrics

In order to follow the performance of machine learning experiments, the project marked certains stage outputs of the data pipeline as metrics. The metrics adopted are: Confusion Matrix and accuracy.

<img src="https://github.com/elvismelo/paper_school_dropout/blob/main/confusion_matrix_model.png" width=30% height=30%>

## Ethical Considerations

In the context of XAI applied to the dropout problem, we're aware that the model does not accurately predict all the reasons that make a student dropping out. As a limitation, we also know that the proportion of the data is insufficient to predict dropout students, due to the unbalance of the target class.

## Caveats and Recommendations

In this work it was used to predict student dropout using a black-box model. Since this is an Education related problem, needs interpretability of its results, such as using XAI frameworks. There are some important issues related to data set imbalances, and that appropriate techniques need to be adopted in order to balance it. For this, artificial data could be generated with class balancing techniques. The one used in this work was the SMOTE technique.
