## 5.6 Explore and Summarize Histories

Exploring history is an important part of Git, and often it is a challenge to find the right commit ID, especially if the commit is from several months ago.

Imagine the ```recipes``` project has more than 50 files. You would like to find a commit that modifies some specific text in ```guacamole.md```. When you type ```git log```, a very long list appeared. How can you narrow down the search?

Recall that the ```git diff``` command allows us to explore one specific file, e.g., ```git diff guacamole.md```. We can apply a similar idea here.

```bash
$ git log guacamole.md
```

Unfortunately some of these commit messages are very ambiguous, e.g., ```update files```. How can you search through these files?

Both ```git diff``` and ```git log``` are very useful and they summarize a different part of the history for you. Is it possible to combine both? Let’s try the following:

```bash
$ git log --patch guacamole.md
```

You should get a long list of output, and you should be able to see both commit messages and the difference between each commit.

Question: What does the following command do?

```bash
$ git log --patch HEAD~9 *.md
```

[Episode 6 Exercise 1](episode6_ex1)
