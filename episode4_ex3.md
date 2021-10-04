## 4.3 Committing Multiple Files

The staging area can hold changes from any number of files that you want to commit as a single snapshot.

1. Add some text to guacamole.md noting the rough price of the ingredients.
1. Create a new file groceries.md with a list of products and their prices for different markets.
1. Add changes from both files to the staging area, and commit those changes.

<details>
  <summary>
        Solution
  </summary>

First we make our changes to the guacamole.md and groceries.md files:

```bash
  $ nano guacamole.md
  $ cat guacamole.md
  ```
```console
  # Ingredients
  - avocado (1.35)
  - lime (0.64)
  - salt (2)
  ```

```bash
  $ nano groceries.md
  $ cat groceries.md
  ```
```console
  # Market A
  - avocado: 1.35 per unit.
  - lime: 0.64 per unit
  - salt: 2 per kg
  ```

 Now you can add both files to the staging area. We can do that in one line:

 ```bash
  $ git add guacamole.md groceries.md
  ```
Or with multiple commands:
  
  ```bash
  $ git add guacamole.md
  $ git add groceries.md
  ```

Now the files are ready to commit. You can check that using ```git status```. If you are ready to commit use:

  ```bash
$ git commit -m "Write prices for ingredients and their source"
  ```
```console
[master cc127c2]
 Write prices for ingredients and their source
 2 files changed, 7 insertions(+)
 create mode 100644 groceries.md

```
  
  [Episode 4 exercise 4](episode4_ex4.md)
