# Conventions and Good Practices

## Code:

1. Variables should be always camel-cased (e.g.: someVariable)
2. CSS module class names should be upper camel cases *(e.g. SomeClass)*
3. Always use verb prefixed names for boolean variables *(e.g.: isActive, hasError)*
4. function and methods variable naming should always reflect an action. Example:
    - **correct:** `getUserInfos()`
    - **wrong:** `userInfos()`
5. Always use semanthic and meaningfull variable names
    - **correct:** `const getUserFullName = (user) => user.fullName;`
    - **wrong:** `const ufn = (u) => u.fullName`
6. Be very specific on variable naming *(e.g.: var user is expected to be an user object and userId to be an user id)*
7. Compound your component final render with small chunks of renders with render functions *(e.g. “renderHeader”, “renderAvatar”, “renderRow”)*
8. Every helper, services and main components should be commented - if possible with usage examples.
9. Use lint and prittier VSCode plugins

## Workflow:

1. In your task manager *(e.g.: Jira)*, always move the issue to the Progress column when you start to work
2. Initiate the activity with the `command: git flow {TASK_TYPE} start {ISSUE_ID}` (use the **issue id** for branch name - e.g.: PRJ-01). For *TASK_TYPE*, you might use the git flow task options “feature”, “bugfix” or “hotfix”
    - Command example: `git flow feature start PRJ-01`
    - Doing that, the branch name should be *feature/VIR-01*
3. When working on the activity, use conventional commits for messages and try to split every commit in a way that each step of your activity will be very descriptive through your commits
    - More informations: https://www.conventionalcommits.org/
    - exemple commit message: *“feat(admin): created layout structure”*
4. When finishing your activity, execute the command: `git flow publish to push your branch`
5. On GitLab/Github, Make a MR/PR for your branch to the develop branch
    - Use the same title from your activity on your task manager *(e.g. Jira)*
    - Prefix the title with tags to give more context, being the first a reference of the *TASK_TYPE* from step 1, and others to give context of the task
      - example: `[FEATURE][ADMIN] Create Admin Panel Layout`
6. Add a link for the related issue
    - example: `Related issue: https://gitlab.com/project/browse/PRJ-01`
7. Add a label that describe the activity
8. On the task manager Activity Issue, add a comment passing the MR link
    - example: `MR: https://gitlab.com/project/frontend/-/merge_requests/1`
