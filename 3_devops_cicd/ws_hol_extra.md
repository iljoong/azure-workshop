# Additional Lab

It is recommend for 2~3 people are working on the same project(repo).

## Prepare Lab

- add members to a working project

## LAB1: Work item

[Reference](https://docs.microsoft.com/en-us/azure/devops/boards/work-items/view-add-work-items?view=azure-devops&tabs=browser)

1. add a work item for each people
    - add a user story (e.g., `add my(alias) controller`)
    - assign user
2. review work items

## LAB2: Branching

[Reference](https://docs.microsoft.com/en-us/azure/devops/repos/git/branch-policies-overview?view=azure-devops
)

1. clone repository
2. create a new branch from Azure DevOps or manually
    ```
    git checkout -b <alias>
    ```
3. add new controller file with your alias, e.g., `apiapp/Controllers/IljoongController.cs`
4. implement controller
5. test locally
6. commit to local repo
    ```
    git add .
    git commit -m "new function"
    ```
7. push to remote repo once you've completed the task
    ```
    git push origin mytask
    ```

> If you have several commits on your branch then you can clean up commits by `squash` or `rebase` before push to remote repo.

## LAB3: Pull request

[Reference](https://docs.microsoft.com/en-us/azure/devops/repos/git/pull-requests-overview?view=azure-devops)

1. submmiter: create a pull request
    - assign a reviwer
2. reviwer: review pull request
3. reviwer: merge branch
4. others: fetch/pull repo
