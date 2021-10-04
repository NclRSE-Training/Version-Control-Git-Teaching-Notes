## 5.3 Understanding Workflow and History

What is the output of the last command in

```bash
$ cd recipes
$ echo "I like tomatos, therefore I like ketchup" > ketchup.md
$ git add ketchup.md
$ echo "ketchup enchances pasta dishes" > ketchup.md
$ git commit -m "my opinions about the red sauce"
$ git checkout HEAD ketchup.md
$ cat ketchup.md # this will print the content of ketchup.md on screen
```

1.
```console
ketchup enchances pasta dishes
```

2.
```console
I like tomatos, therefore I like ketchup
```

3.
```console
I like tomatos, therefore I like ketchup
ketchup enchances pasta dishes
```

4.
```console
Error because you have changed ketchup.md without committing the changes
```

<details>
  <summary>
Solution
  </summary>

The answer is 2.

The changes to the file from the second ```echo``` command are only applied to the working copy, The command ```git add ketchup.md``` places the current version of ```ketchup.md``` into the staging area. not the version in the staging area.

So, when ```git commit -m "my opinions about the red sauce"``` is executed, the version of ```ketchup.md``` committed to the repository is the one from the staging area and has only one line.

At this time, the working copy still has the second line (and

```git status``` will show that the file is modified). However, ```git checkout HEAD ketchup.md``` replaces the working copy with the most recently committed version of ```ketchup.md```. So, ```cat ketchup.md``` will output

```console
I like tomatos, therefore I like ketchup
  ```
  
  </details>
  
[Episode 5 exercise 4](episode5_ex4.md)

