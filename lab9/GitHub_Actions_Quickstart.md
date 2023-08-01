# GitHub Actions

## Reading Official Guide

I followed the official quickstart guide at https://docs.github.com/en/actions/quickstart

**Key learnings:**

-   GitHub Actions help automate software workflows directly in the repo
-   Workflows are defined as YAML files in .github/workflows directory
-   A workflow contains one or more jobs that run in sequence or in parallel
-   Jobs contain steps that are individual tasks/commands
-   We can write custom steps or use pre-built actions from GitHub Marketplace
-   The workflow runs when triggered by an event like push, pull request etc
-   GitHub provides Linux, Windows and Mac virtual machines to run workflows
-   Environment variables are available to access repo details
-   Workflow execution results are displayed on GitHub and can be monitored

To get started, I created a simple workflow YAML that prints "Hello World" on push using the `actions/checkout` and `actions/setup-node` pre-built actions.

## Observing Execution

On pushing a commit to trigger the workflow, I can see the execution on the Actions tab.
It ran successfully in under a minute and I can expand to see the steps and output of each step:

```bash
Run actions/checkout@v3
Run actions/setup-node@v3
  with:
    node-version: '18'
Run echo "Hello World"
Hello World
```

I also triggered a failure by introducing an error. This turned the workflow status to red. The logs clearly showed the error steps.
GitHub Actions provides nice visibility into automating workflows directly in the repository. Workflows can be monitored, tweaked and debugged right within GitHub.
