
## 6.6 Log Files

You wrote a script that creates many intermediate ```log-files``` of the form ```log_01```, ```log_02```, ```log_03```, etc. You want to keep them but you do not want to track them through ```git```.

1. Write one ```.gitignore``` entry that excludes files of the form ```log_0```1, ```log_02```, etc.
1. Test your “ignore pattern” by creating some dummy files of the form ```log_01```, etc.
1. You find that the file ```log_01``` is very important after all, add it to the tracked files without changing the ```.gitignore``` again.
1. Discuss with your neighbor what other types of files could reside in your directory that you do not want to track and thus would exclude via ```.gitignore```.

<details>
  <summary>
Solution
  </summary>

append either ```log_*``` or ```log*``` as a new entry in your .gitignore
track ```log_01``` using ```git add -f log_01```

</details>
