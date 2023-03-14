# Pedefined vars preset in the job 

## Example to show them 

```
stages:
  - build 
  
show_env:
  stage: build 
  scripts:
    - env 
    - pwd 
    - ls -la


```



## Reference 

  * https://docs.gitlab.com/ee/ci/variables/predefined_variables.html
