# Code Quality 

```
15. Code Quality Testing 

Schritt 0: Prerequisites 

If you’re using shared runners, the Code Quality job must be configured for the Docker-in-Docker workflow.
If you’re using private runners, you should use an alternative configuration recommended for running Code Quality analysis more efficiently.
The runner must have enough disk space to store the generated Code Quality files. For example, on the GitLab project the files are approximately 7 GB.


Schritt 1:
jquery/jquery import
https://github.com/jquery/jquery.git
repo - name
jm-jquery 


Schritt 2:
# hier auch vorstellen, dass das jobs sind, die bereits
# vorkonfiguriert sind in git 

include:
  - template: Code-Quality.gitlab-ci.yml




Referenz:
https://docs.gitlab.com/ee/ci/testing/code_quality.html
Achtung: Nicht alle Funktionen sind im Free - Tier freigeschaltet 
-> nur merge request widget 

Schritt 3:
merge requests changes view
und pipleline changes view 
vorstellen. 

15. Code Quality Testing - vollständigen code ansehen 

--> ci/cd -> editor -> see merged yaml 


16. Adjust to merge_request_event // no branch pipeline 

include:
   - template: Code-Quality.gitlab-ci.yml


# overwrite parts of the include 
code_quality:
  rules:
  - if: "$CODE_QUALITY_DISABLED"
    when: never
  - if: $CI_PIPELINE_SOURCE == 'merge_request_event'


also set checkbox to only merge when pipeline suceeds 
in Project -> Settings -> Merge_request


Now make a change in README.md and save it in feature/4813 
after that make a merge request


```
