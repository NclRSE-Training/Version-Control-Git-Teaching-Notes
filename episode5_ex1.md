
## 5.1 Recovering Older Versions of a File

Jennifer has made changes to the Python script that she has been working on for weeks, and the modifications she made this morning “broke” the script and it no longer runs. She has spent ~ 1hr trying to fix it, with no luck…

    Luckily, she has been keeping track of her project’s versions using Git! Which commands below will let her recover the last committed version of her Python script called ```data_cruncher.py```?

1. ```$ git checkout HEAD```

1. ```$ git checkout HEAD data_cruncher.py```

1. ```$ git checkout HEAD~1 data_cruncher.py```

1. ```$ git checkout <unique ID of last commit> data_cruncher.py```

1. Both 2 and 4

<details>
  <summary>
        Solution
  </summary>

The answer is (5)-Both 2 and 4.

The ```checkout``` command restores files from the repository, overwriting the files in your working directory. Answers 2 and 4 both restore the latest version in the repository of the file ```data_cruncher.py```. Answer 2 uses ```HEAD``` to indicate the latest, whereas answer 4 uses the unique ID of the last commit, which is what ```HEAD``` means.

Answer 3 gets the version of ```data_cruncher.py``` from the commit before ```HEAD```, which is NOT what we wanted.

Answer 1 can be dangerous! Without a filename, ```git checkout``` will restore all files in the current directory (and all directories below it) to their state at the commit specified. This command will restore ```data_cruncher.py``` to the latest commit version, but it will also restore any other files that are changed to that version, erasing any changes you may have made to those files! As discussed above, you are left in a detached ```HEAD``` state, and you don’t want to be there.
</details>

[Episode 5 exercise 2](episode5_ex2.md)
