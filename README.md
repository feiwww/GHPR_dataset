# Introduction

The GHPR dataset identify defect information based on PRs in the Github workflow, Previous studies identified defective source code parts by git commits or issues on GitHub, but many descriptions of commits (or issues) are not well-formed, which adds noise to defect datasets. We believe that the defect information with team review and the GitHub workflow is more accurate. 

## data

<table>
   <tr>
      <td>Data Name</td>
      <td>Type</td>
      <td>Description</td>
   </tr>
   <tr>
      <td>Project Name</td>
      <td>Project Information</td>
      <td>The name of the project</td>
   </tr>
   <tr>
      <td>Project Owner</td>
      <td></td>
      <td>The owner of the project</td>
   </tr>
   <tr>
      <td>Language</td>
      <td></td>
      <td>The programming of the project</td>
   </tr>
   <tr>
      <td>Git_Address</td>
      <td></td>
      <td>The git adderss of the project</td>
   </tr>
   <tr>
      <td>Project Description</td>
      <td></td>
      <td>The description of the project provided by the owner</td>
   </tr>
   <tr>
      <td>Project Label</td>
      <td></td>
      <td>The label of the project provided by the owner</td>
   </tr>
   <tr>
      <td>PR Title</td>
      <td>PRs information from remote repository</td>
      <td>The title of the defect related PR</td>
   </tr>
   <tr>
      <td>PR Description</td>
      <td></td>
      <td>The description of the defect related PR</td>
   </tr>
   <tr>
      <td>SHA New</td>
      <td></td>
      <td>The ID of the version after the defect being fixed</td>
   </tr>
   <tr>
      <td>SHA Old</td>
      <td></td>
      <td>The ID of the version before the defect being fixed</td>
   </tr>
   <tr>
      <td>Path</td>
      <td></td>
      <td>The path of the changed files between the version before/after fixed</td>
   </tr>
   <tr>
      <td>Content_New</td>
      <td>Defect related Code</td>
      <td>The content of the related files after the defecr being fixed</td>
   </tr>
   <tr>
      <td>Content_Old</td>
      <td></td>
      <td>The content of the related files before the defecr being fixed</td>
   </tr>
   <tr>
      <td>Defect Code</td>
      <td></td>
      <td>The defect code we recognize from the content of the related files content</td>
   </tr>
   <tr>
      <td></td>
   </tr>
</table>

## Requirements


## Quick Start

.csv and .sql

## References
Please cite our paper if you use this dataset in your own work:
