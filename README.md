# GHPR dataset

The GHPR dataset is used in our empirical studies and evaluation. We identify 3026 bug fixing based on Pull Requests(PRs) in Github. If treat the defective and fixed version in each bug fixing as two instances, our GHPR dataset have 3026 defective instance and 3026 non-defective instance. 

Previous studies identified defective source code parts by git commits or issues on GitHub, but many descriptions of commits (or issues) are not well-formed, which adds noise to defect datasets. We believe that the defect information with team review and the GitHub workflow is more accurate. 


## Quick Start

Two formats of the GHPR datset are provided:

1. ghprdata.csv
2. ghprdata.sql

The CSV file can be imported into Python using numpy or pandas. For more convenient used in database management system(e.g. MySQL), we also provide a SQl file of which the character set is utf-8.


## data
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



# References
Please cite our paper if you use this dataset in your publication:
