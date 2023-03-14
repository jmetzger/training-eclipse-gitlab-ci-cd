image: busybox:1.36

stages:          # List of stages for jobs, and their order of execution
  - build
  - test
  - deploy

job:
  stage: test
  script: 
    - echo "Hello, Rules!"
    - echo "$FEATURE_FLAG_UI"
    - echo "$MASTER_CONFIG"
    - cat $MASTER_CONFIG

