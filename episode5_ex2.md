## 5.2 Reverting a Commit

Jennifer is collaborating on her Python script with her colleagues and realizes her last commit to the project’s repository contained an error and she wants to undo it. ```git revert [erroneous commit ID]``` will create a new commit that reverses Jennifer’s erroneous commit. Therefore ```git revert``` is different to ```git checkout [commit ID]``` because git checkout returns the files within the local repository to a previous state, whereas ```git revert``` reverses changes committed to the local and project repositories.

Below are the right steps and explanations for Jennifer to use ```git revert```, what is the missing command?

1. ``` ________ # Look at the git history of the project to find the commit ID```
1. Copy the ID (the first few characters of the ID, e.g. 0b1d055).
1. ```git revert [commit ID]```
1. Type in the new commit message.
1. Save and close

<details>
  <summary>
    Solution
  </summary>
  
  <pre><code>git log --graph --oneline</code></pre>
  
</details>

[Episode 5 Exercise 3](episode5_ex3.md)
