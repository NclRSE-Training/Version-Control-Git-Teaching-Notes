## 7.4 GitHub License and README files

In this section we learned about creating a remote repository on GitHub, but when you initialized your GitHub repo, you didn’t add a README.md or a license file. If you had, what do you think would have happened when you tried to link your local and remote repositories?

<details>
  <summary>
    Solution
  </summary>

  <p>
    In this case, we’d see a merge conflict due to unrelated histories. When GitHub creates a README.md file, it performs a commit in the remote repository. When you try to pull the remote repository to your local repository, Git detects that they have histories that do not share a common origin and refuses to merge.
  </p>

  <pre><code>$ git pull origin master</code></pre>

  <pre><code>warning: no common commits
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
From https://github.com/alflin/recipes
* branch            master     -> FETCH_HEAD
* [new branch]      master     -> origin/master
fatal: refusing to merge unrelated histories</code></pre>

  <p>
    You can force git to merge the two repositories with the option <code>--allow-unrelated-histories</code>. Be careful when you use this option and carefully examine the contents of local and remote repositories before merging.
  </p>

  <pre><code>$ git pull --allow-unrelated-histories origin master</code></pre>

  <pre><code>From https://github.com/alflin/recipes
* branch            master     -> FETCH_HEAD
Merge made by the 'recursive' strategy.
README.md | 1 +
1 file changed, 1 insertion(+)
create mode 100644 README.md</code></pre>

</details>

[Episode 8 Exercise 1](episode8_ex1)
