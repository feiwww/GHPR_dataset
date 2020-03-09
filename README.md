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
| Feature               | Description                                                             |
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
We calculate 21 static metrics for the total 6052 instances in GHPR dataset, which is the data used for the baseline approaches. All metrics were calculated by the open-source tool [mauricioaniche/ck](https://github.com/mauricioaniche/ck). The description of the metrics as fellow.
| Feature              | Description                                                                                                                                          |
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| CBO                  | Coupling between objects\. Counts the number of dependencies a class has\.                                                                           |
| WMC                  | Weight Method Class or McCabe's complexity\. It counts the number of branch instructions in a class\.                                                |
| DIT                  | Depth Inheritance Tree\. It counts the number of "fathers" a class has\. All classes have DIT at least 1 \(everyone inherits java\.lang\.Object\)\.  |
| rfc                  | Response for a Class\. Counts the number of unique method invocations in a class\.                                                                   |
| lcom                 | Lack of Cohesion of Methods\. Calculates LCOM metric\.                                                                                               |
| totalMethods         | Counts the number of methods\.                                                                                                                       |
| totalFields          | Counts the number of fields\.                                                                                                                        |
| NOSI                 | Number of static invocations\. Counts the number of invocations to static methods\.                                                                  |
| LOC                  | Lines of code\. It counts the lines of count, ignoring empty lines\.                                                                                 |
| returnQty            | Quantity of returns\. The number of return instructions\.                                                                                            |
| loopQty              | Quantity of loops\. The number of loops \(i\.e\., for, while, do while, enhanced for\)\.                                                             |
| comparisonsQty       | Quantity of comparisons\. The number of comparisons \(i\.e\., == and \!=\)\.                                                                         |
| tryCatchQty          | Quantity of try/catches\. The number of try/catches\.                                                                                                |
| parenthesizedExpsQty | Quantity of parenthesized expressions\. The number of expressions inside parenthesis\.                                                               |
| stringLiteralsQty    | String literals\. The number of string literals \(e\.g\., "John Doe"\)\.                                                                             |
| numbersQty           | Quantity of Number\. The number of numbers \(i\.e\., int, long, double, float\) literals\.                                                           |
| assignmentsQty       | Quantity of Variables\. Number of declared variables\.                                                                                               |
| mathOperationsQty    | Quantity of Math Operations: The number of math operations \(times, divide, remainder, plus, minus, left shit, right shift\)\.                       |
| variablesQty         | Quantity of Variables\. Number of declared variables\.                                                                                               |
| maxNestedBlocks      | Max nested blocks\. The highest number of blocks nested together\.                                                                                   |
| uniqueWordsQty       | Number of unique words\. Number of unique words in the source code\.                                                                                 |



# References
Please cite our paper if you use this dataset in your publication:
@ARTICLE{***, 
author={Wang Fei and Ai Jun and Xu Jiaxi}, 
journal={IEEE Transactions on Software Engineering}, 
title={Software Defect Prediction Based on Graph Representation Learning}, 
year={2020}, }
