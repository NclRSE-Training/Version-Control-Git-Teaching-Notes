
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

The ```!``` modifier will negate an entry from a previously defined ignore pattern. Because the ```!*.dat``` entry negates all of the previous ```.dat``` files in the ```.gitignore```, none of them will be ignored, and all ```.dat``` files will be tracked.

</details>

[Episode 6 exercise 6](episode6_ex6.md)
