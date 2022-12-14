## Development Policy

You will find below all the best practices to adopt by contributing to the project.

### Commit Policy

Your commits should follow the following format:

> \[Symbol\] Verb Description #IssueNumber

| Symbol | Meaning  |
| :-----: | :-: |
| + | Addition |
| - | Deletion |
| * | Modification |

For example :

```bash
    git commit -m "[+] Implement readme.md commit policy table #12"
```

Any commit that does not meet this standard will not be deleted. Just be careful.

It is recommended to commit on a regular basis.

### Branch Policy

Your branch should follow the following format:

> Issue/Which/I/Refer/To/IssueNumber

For example :

```bash
    git checkout -b Architecture/Setup/Readme/12
```

Any branch that does not respect this format will be refused all of its associated PRs.

Please make one branch per issue.

Try to push as regularly as possible so everyone can see where you are at.

### Pull Request Policy

It is necessary to make at least one pull request per branch.

When creating a pull request, please follow the same standard as for branches.

Please briefly describe all the features contained in the PR.

Prioritize verbal dialogue during your reviews instead of putting a lot of comments.

Try not to exceed 24 hours before reading your PRs.

It is obviously forbidden to approve a merge until all the reviewers have accepted the PR as well as the success of the workflows.

### Issue Policy

When identifying a new functionality, it is necessary to create a new issue respecting the following format:

* The name of the issue must correspond to the part of the code concerned

```bash
    Name : Architecture - Setup - Add the Readme
```

* Try to describe as much as possible in the issue the modifications that it will apply in the project.

* Add the different labels according to the table below :

| Label | Meaning |
| :-----: | :-: |
| Implementing | Add a new feature |
| Refactoring | Change an actual feature |
| Question | An interrogation on the subject |
| Help | Need some help on the issue |
| Pull Request | Refere to a PR |
| Bug | Signal a bug on the project |
| Documentation | Create some technical documentation |

* Normally all the issues will be moved into the projects automatically.

### HotFix Policy

When you encounter a bug :

* If the bug relates to the feature you are working on, you can fix it directly in your branch.

* Otherwise, it will be necessary to create an issue explaining the nature of the bug and to associate the bug label with it. You can then fix the bug by creating a new branch and requesting a review from the creator of the affected feature.

Your HotFix branch must follow the following format :

> Hotfix/Functionnality/Wich/I/Refer/To/IssueNumber

```bash
    git checkout -b HotFix/Architecture/Setup/Readme/14
```

### Testing Policy

You are asked to try to practice Test Driven Development, which basically consists of carrying out tests before the realization of the associated source code.

Any PR not being a minimum tested will be refused, regardless of the language used.

For carrying out tests in C and C++, refer to the Tests Template located inside the tests folder.

### Documentation Policy

We using Doxygen for documentation, and in order to allow the proper deployment of the documentation, please respect the following protocol:

* Please add the \file at the top of each of your files :

```bash
    /// \file path/from/the/repository/root.h
```

* Please document your defines and typedefs as follows :

```bash
    ///
    /// \brief I'm a basic define wich say hello 
    ///
```

* Please document your functions in the .h as follows:

```bash
    ///
    /// \brief I'm a basic function wich print hello
    ///
    /// \param str I'm the first param and i'm the string to display
    /// \return int The success value
    ///
```

* No functions should have documentation within .c/.cpp files except static functions.

Any undocumented elements will lead to the refusal of the PR.