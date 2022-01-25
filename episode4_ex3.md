## 4.3 Committing Multiple Files

The staging area can hold changes from any number of files that you want to commit as a single snapshot.

1. Add some text to ```guacamole.md``` noting the rough price of the ingredients.
1. Create a new file ```groceries.md``` with a list of products and their prices for different markets.
1. Add changes from both files to the staging area, and commit those changes.

<details>
  <summary>
Solution
  </summary>

  <p>
    First we make our changes to the <code>guacamole.md</code> and <code>groceries.md</code> files:
  </p>

  <pre><code>$ nano guacamole.md
$ cat guacamole.md</code></pre>
  
  <pre><code># Ingredients
- avocado (1.35)
- lime (0.64)
- salt (2)</code></pre>

  <pre><code>$ nano groceries.md
$ cat groceries.md</code></pre>
  
  <pre><code># Market A
- avocado: 1.35 per unit.
- lime: 0.64 per unit
- salt: 2 per kg</code></pre>

  <p>
    Now you can add both files to the staging area. We can do that in one line:
  </p>

<pre><code>$ git add guacamole.md groceries.md</code></pre>
  
  <p>
    Or with multiple commands:
  </p>
  
  <pre><code>$ git add guacamole.md
$ git add groceries.md</code></pre>

  <p>
    Now the files are ready to commit. You can check that using <code>git status</code>. If you are ready to commit use:
  </p>

  <pre><code>$ git commit -m "Write prices for ingredients and their source"</code></pre>

  <pre><code>[master cc127c2]
 Write prices for ingredients and their source
 2 files changed, 7 insertions(+)
 create mode 100644 groceries.md</code></pre>

</details>
  
[Episode 4 Exercise 4](episode4_ex4.md)
