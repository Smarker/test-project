# Synchronize DevOps and Github Repositories

These directions are largely derived from
[this post](https://stackoverflow.com/questions/36814023/how-to-synchronize-vsts-and-github-respositories-when-commits-are-made).

1. Create repo in DevOps.
    * Create a variable group specifying these secret values:
      * a github personal access token
      * a devops personal access token
1. Create an empty repo in Github with the same name as the one in DevOps.

When code is pushed to the `master` branch of DevOps, both
`devops-master-updated-pipelines.yml` and `github-master-updated-pipelines.yml`
pipelines will be triggered.
