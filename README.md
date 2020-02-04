# Synchronize DevOps and Github Repositories

These directions are largely derived from
[this post](https://stackoverflow.com/questions/36814023/how-to-synchronize-vsts-and-github-respositories-when-commits-are-made).

1. Create repo in DevOps.
    * Create a variable group specifying these secret values:
      * a github personal access token
      * a devops personal access token
1. Create an empty repo in Github with the same name as the one in DevOps.

## Updating Github with DevOps Changes

When code is pushed to `master` the `devops-master-updated-pipelines.yml`
pipeline will be triggered. This pipeline will pull the latest changes from
github before pushing the devops code changes to github.

## Updating DevOps with Github Changes

Manually trigger the `github-master-updated-pipelines.yml` pipeline to fetch
the latest changes from github.
