# Working with rules 

## Example 1 

```
job:
  script: echo "Hello, Rules!"
  rules:
    - if: $CI_PIPELINE_SOURCE == "merge_request_event"
      when: manual
      allow_failure: true

```

## Ref:

  * https://docs.gitlab.com/ee/ci/jobs/job_control.html#specify-when-jobs-run-with-rules
