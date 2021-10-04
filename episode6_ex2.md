
## 6.2 Including Specific Files

How would you ignore all ```.png``` files in your root directory except for ```final.png```? Hint: Find out what ! (the exclamation point operator) does

<details>
  <summary>
Solution
  </summary>

You would add the following two lines to your .gitignore:

  ```console
*.png           # ignore all png files
!final.png      # except final.png
  ```

The exclamation point operator will include a previously excluded entry.

Note also that because you’ve previously committed ```.png``` files in this lesson they will not be ignored with this new rule. Only future additions of ```.png``` files added to the root directory will be ignored.

</details>

[Episode 6 exercise 3](episode6_ex3.md)
