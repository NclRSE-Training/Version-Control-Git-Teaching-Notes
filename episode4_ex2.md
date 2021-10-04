
## 4.2 Committing Changes to Git

Which command(s) below would save the changes of myfile.txt to my local Git repository?

1. 
```bash
$ git commit -m "my recent changes"
```
2.
```bash
$ git init myfile.txt
$ git commit -m "my recent changes"
```
3.
```bash
$ git add myfile.txt
$ git commit -m "my recent changes"
```
4.
```bash
$ git commit -m myfile.txt "my recent changes"
```

<details>
  <summary>
    Solution
  </summary>
  
1. Would only create a commit if files have already been staged.
1. Would try to create a new repository.
1. Is correct: first add the file to the staging area, then commit.
1. Would try to commit a file “my recent changes” with the message myfile.txt.
  </details>

[Episode 4 exercise 3](episode4_ex3.md)
