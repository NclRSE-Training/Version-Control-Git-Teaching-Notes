
## 6.2 Including Specific Files

How would you ignore all ```.png``` files in your root directory except for ```final.png```? Hint: Find out what ```!``` (the exclamation point operator) does

<details>
  <summary>
Solution
  </summary>
  
  <p>
    You would add the following two lines to your <code>.gitignore</code>:
  </p>
  
  <pre><code>*.png           # ignore all png files
!final.png      # except final.png</code></pre>

  <p>
The exclamation point operator will include a previously excluded entry.
  </p>
  <p>
Note also that because you’ve previously committed <code>.png</code> files in this lesson they will not be ignored with this new rule. Only future additions of <code>.png</code> files added to the root directory will be ignored.
  </p>
  
</details>

[Episode 6 exercise 3](episode6_ex3.md)
