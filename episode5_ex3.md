## 5.3 Understanding Workflow and History

What is the output of the last command in

```bash
$ cd recipes
$ echo "I like tomatos, therefore I like ketchup" > ketchup.md
$ git add ketchup.md
$ echo "ketchup enchances pasta dishes" > ketchup.md
$ git commit -m "my opinions about the red sauce"
$ git checkout HEAD ketchup.md
$ cat ketchup.md # this will print the content of ketchup.md on screen
```

<ol>
  <li><pre><code>ketchup enchances pasta dishes</code></pre></li>
  <li><pre><code>I like tomatos, therefore I like ketchup</code></pre></li>
  <li><pre><code>I like tomatos, therefore I like ketchup
ketchup enchances pasta dishes</code></pre></li>
  <li><pre><code>Error because you have changed ketchup.md without committing the changes</code></pre></li>
</ol>

<details>
  <summary>
    Solution
  </summary>

  <p>
    The answer is 2.
  </p>
  <p>
    The changes to the file from the second <code>echo</code> command are only applied to the working copy, The command <code>git add ketchup.md</code> places the current version of <code>ketchup.md</code> into the staging area. not the version in the staging area.
  </p>
  <p>
    So, when <code>git commit -m "my opinions about the red sauce"</code> is executed, the version of <code>ketchup.md</code> committed to the repository is the one from the staging area and has only one line.
  </p>
  <p>
    At this time, the working copy still has the second line (and <code>git status</code> will show that the file is modified). However, <code>git checkout HEAD ketchup.md</code> replaces the working copy with the most recently committed version of <code>ketchup.md</code>. So, <code>cat ketchup.md</code> will output:
  </p>

  <pre><code>I like tomatos, therefore I like ketchup</code></pre>
  
</details>
  
[Episode 5 Exercise 4](episode5_ex4.md)
