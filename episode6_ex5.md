## The Order of Rules

Given a ```.gitignore``` file with the following contents:

```console
*.dat
!*.dat
```

What will be the result?

<details>
  <summary>
    Solution
  </summary>

  <p>
    The <code>!</code> modifier will negate an entry from a previously defined ignore pattern. Because the <code>!*.dat</code> entry negates all of the previous <code>.dat</code> files in the <code>.gitignore</code>, none of them will be ignored, and all <code>.dat</code> files will be tracked.
  </p>
    
</details>

[Episode 6 Exercise 6](episode6_ex6.md)
