
## 6.1 Ignoring Nested Files

Given a directory structure that looks like:

```console
receipts/data
receipts/plots
```

How would you ignore only ```receipts/plots``` and not ```receipts/data```?

<details>
  <summary>
Solution
  </summary>

If you only want to ignore the contents of <code>receipts/plots</code>, you can change your <code>gitignore</code> to ignore only the <code>/plots/</code> subfolder by adding the following line to your <code>.gitignore</code>:<br/>

  <pre><code>receipts/plots/</code></pre>
  
  <p>
This line will ensure only the contents of <code>receipts/plots</code> is ignored, and not the contents of <code>receipts/data</code>
  </p>
  <p>
As with most programming issues, there are a few alternative ways that one may ensure this ignore rule is followed. The “Ignoring Nested Files: Variation” exercise has a slightly different directory structure that presents an alternative solution. Further, the discussion page has more detail on ignore rules.
  </p>
</details>
  
[Episode 6 exercise 2](episode6_ex2.md)
