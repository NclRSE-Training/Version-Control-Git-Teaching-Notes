
## 3.1 Places to Create Git Repositories

Along with tracking information about recipes (the project we have already created), Alfredo would also like to track information about cocktails. Despite Jimmy’s concerns, Alfredo creates a cocktails project inside his recipes project with the following sequence of commands:

```bash
$ cd ~/Desktop    # return to Desktop directory
$ cd recipes      # go into recipes directory, which is already a Git repository
$ ls -a           # ensure the .git subdirectory is still present in the recipes directory
$ mkdir cocktails # make a sub-directory recipes/cocktails
$ cd cocktails    # go into cocktails subdirectory
$ git init        # make the cocktails subdirectory a Git repository
$ ls -a           # ensure the .git subdirectory is present indicating we have created a new Git repository
```
Is the ```git init``` command, run inside the ```cocktails``` subdirectory, required for tracking files stored in the ```cocktails``` subdirectory?

<details>
<summary>
  Solution
</summary>

  <p>
No. Alfredo does not need to make the cocktails subdirectory a Git repository because the recipes repository will track all files, sub-directories, and subdirectory files under the recipes directory. Thus, in order to track all information about cocktails, Alfredo only needed to add the cocktails subdirectory to the recipes directory.
  </p><p>
Additionally, Git repositories can interfere with each other if they are “nested”: the outer repository will try to version-control the inner repository. Therefore, it’s best to create each new Git repository in a separate directory. To be sure that there is no conflicting repository in the directory, check the output of git status. If it looks like the following, you are good to go to create a new repository as shown above:
  </p>
<pre>
$ git status
</pre>

<pre>
fatal: Not a git repository (or any of the parent directories): .git
</pre>
</details>

  [Episode 3 exercise 2](episode3_ex2.md)
