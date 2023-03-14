# Working with rules 

## Example 1 

```
job:
  stage: test
  script: echo "Hello, Rules!"
  rules:
    - if: $CI_PIPELINE_SOURCE == "merge_request_event"
      when: manual
      allow_failure: true

```

```
Prepare:
1. gitlab-ci.yml oben entsprechend anpassen 
```

```
# Test 1
2. Ändern wir die README.md -> und im master branch committen 
3. wie verhält sich die Pipeline ?
```

```
# Test 2

2. Ändern wir die README.md -> und in einen neuen Feature-branch committen 
3. merge-request 
```

## Ref:

  * https://docs.gitlab.com/ee/ci/jobs/job_control.html#specify-when-jobs-run-with-rules
