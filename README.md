# GHPR Dataset: A Dataset for Software Defect Prediction

The GHPR dataset is used in our empirical studies and evaluation. We identify 3026 bug fixing based on Pull Requests(PRs) in Github. Each bug fixing is treated as a record in the dataset. 

From the view of supervised learning, we can consider the defective and fixed file version in each record as two learning instances. the GHPR dataset totally have 6052 learning instances which contain 3026 defective instances and 3026 non-defective instances.  

## Data Format
Two publication formats are provided in *ghprdata.zip*:

1. ghprdata.csv
2. ghprdata.sql

The CSV file is simple and well-supported in Python using numpy or pandas. Because the databases support large datasets better than CSV files do, we also provide a SQL file of which the character set is utf-8.

## Data Feature
Each record includes the following 16 features.
| Label               | Description                                                             |
|---------------------|-------------------------------------------------------------------------|
| PROJECT_NAME        | The name of the project                                                 |
| PROJECT_OWNER       | The owner of the project                                                |
| PROJECT_DESCRIPTION | The description of the project provided by the owner                    |
| PROJECT_LABEL       | The label of the project provided by the owner                          |
| PROJECT_LANGUAGE    | The programming language of the project                                 |
| SHA_FIXED           | The ID of the version after the defect being fixed                      |
| SHA_BUG             | The ID of the version before the defect being fixed                     |
| DIFF_CODE           | The defect-related code we recognize from the content of the fixed file |
| COMMIT_DESCRIPTION  | The description of the commit in the defect-related PR                  |
| COMMIT_TIME         | The time of the commit in the defect-related PR                         |
| OLD_CONTENT         | The content of the defect-related file before defects being fixed       |
| NEW_CONTENT         | The content of the defect-related file after defects being fixed        |
| OLD_PATH            | The old path of the changed files                                       |
| NEW_PATH            | The new path of the changed files                                       |
| PR_TITLE            | The title of the defect related PR                                      |
| PR_DESCRIPTION      | The description of the defect related PR                                |

# baseline
We calculate 21 static metrics for the total 6052 instances in GHPR dataset, which is the data used for the baseline approaches. All metrics were calculated by the open-source tool *mauricioaniche/ck*. The description of the metrics can be found in the [repository](https://github.com/mauricioaniche/ck).

# References
Please cite our paper if you use this dataset in your publication:
