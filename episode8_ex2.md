## 8.2 Review Changes

The Owner pushed commits to the repository without giving any information to the Collaborator. How can the Collaborator find out what has changed with command line? And on GitHub?

<details>
  <summary>
    Solution
  </summary>

  <p>
    On the command line, the Collaborator can use <code>git fetch origin master</code> to get the remote changes into the local repository, but without merging them. Then by running <code>git diff master origin/master</code> the Collaborator will see the changes output in the terminal.
  </p>
  <p>
    On GitHub, the Collaborator can go to the repository and click on “commits” to view the most recent commits pushed to the repository.
  </p>
  
</details>

[Episode 8 Exercise 3](episode8_ex3.md)
