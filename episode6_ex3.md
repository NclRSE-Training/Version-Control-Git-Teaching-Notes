
## 6.3 Ignoring Nested Files: Variation

Given a directory structure that looks similar to the earlier Nested Files exercise, but with a slightly different directory structure:

```console
receipts/data
receipts/images
receipts/plots
receipts/analysis
```

How would you ignore all of the contents in the receipts folder, but not ```receipts/data```?

Hint: think a bit about how you created an exception with the ```!``` operator before.


<details>
  <summary>
Solution
  </summary>

  <p>
    If you want to ignore the contents of <code>receipts/</code> but not those of <code>receipts/data/</code>, you can change your <code>.gitignore</code> to ignore the contents of <code>receipts</code> folder, but create an exception for the contents of the <code>receipts/data</code> subfolder. Your <code>.gitignore</code> would look like this:
  </p>
  
  <pre><code>receipts/*               # ignore everything in receipts folder
!receipts/data/          # do not ignore receipts/data/ contents</code></pre>

</details>

[Episode 6 exercise 4](episode6_ex4.md)
