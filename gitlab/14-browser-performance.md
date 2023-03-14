# Browser Performance Testing

```
geht nicht in free tier.
https://docs.gitlab.com/ee/ci/testing/browser_performance_testing.html

unter der Haube wir site speed verwendet.

include:
  template: Verify/Browser-Performance.gitlab-ci.yml

browser_performance:
  variables:
    URL: https://example.com


Job muss einmal durchgelaufen sein, damit verglichne werden kann.

Verwendet dieses Plugin, um daten als json bereitzustellen. 

---->
First, define a job in your .gitlab-ci.yml file that generates the Browser Performance report artifact. GitLab then checks this report, compares key performance metrics for each page between the source and target branches, and shows the information in the merge request.
<----

https://docs.gitlab.com/ee/ci/testing/img/browser_performance_testing.png
```
