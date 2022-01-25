## 7.1 GitHub GUI

Browse to your ```recipes``` repository on GitHub. Under the Code tab, find and click on the text that says “XX commits” (where “XX” is some number). Hover over, and click on, the three buttons to the right of each commit. What information can you gather/explore from these buttons? How would you get that same information in the shell?

<details>
  <summary>
    Solution
  </summary>

  <p>
    The left-most button (with the picture of a clipboard) copies the full identifier of the commit to the clipboard. In the shell, <code>git log</code> will show you the full commit identifier for each commit.
  </p>
  <p>
    When you click on the middle button, you’ll see all of the changes that were made in that particular commit. Green shaded lines indicate additions and red ones removals. In the shell we can do the same thing with <code>git diff</code>. In particular, <code>git diff ID1..ID2</code> where ID1 and ID2 are commit identifiers (e.g. <code>git diff a3bf1e5..041e637</code>) will show the differences between those two commits.
  </p>
  <p>
    The right-most button lets you view all of the files in the repository at the time of that commit. To do this in the shell, we’d need to checkout the repository at that particular time. We can do this with <code>git checkout ID</code> where ID is the identifier of the commit we want to look at. If we do this, we need to remember to put the repository back to the right state afterwards!
  </p>
  
</details>

[Episode 7 Exercise 2](episode7_ex2.md)
