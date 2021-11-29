## Overview
When something happens (Events) IN or TO the repository, aumation actions are executed in response.

### Events: Pull Request creation, Issue creation, Contributor Join, Pull Request Merge, Other apps events

### Workflow
=> Listen To Events
=> Trigger Something (Actions) like, Sort, Label, Assign it, Reproduce etc. Togather Actions are workflow.

### CI/CD (Continuous Integration and Delivery) Pipeline:
=> Most common workflow for personal repo. Commit code, Test, Build, Push, Deploy etc.
=> No Thirdparty (Jenkins), Github's own tech
=> lots of tools for integration with other technologies.
=> Boilerplates for integration

### Syntax of the workflow file:
=> 

```yaml
name: soem_name # optional, used by yourself

on: # required | events
 push: 
  branches: [master]
 pull_request:
  branches: [master]


jobs: # required | executes everytime on event match | one or more jobs
 build:
  runs-on: ubuntu-latest
  steps:
   - uses: actions/checkout@2
   - name: Set up something
     uses: another-action-script
     with:
        version: 1.4
   - name: another-name
     run: chmod +x gradlew # linux command
   - name: another-name
     run: ./gradlew build | # linux command
            andther-command | # pipe used for multiline command in yaml
            another_command
```