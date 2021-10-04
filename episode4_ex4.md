
## 4.4 ```bio``` Repository

- Create a new Git repository on your computer called bio.
- Write a three-line biography for yourself in a file called me.txt, commit your changes
- Modify one line, add a fourth line
- Display the differences between its updated state and its original state.

<details>
  <summary>
Solution
  </summary>

If needed, move out of the ```recipes``` folder:

  ```bash
$ cd ..
  ```

Create a new folder called ```bio``` and ‘move’ into it:

  ```bash
$ mkdir bio
$ cd bio
  ```

Initialise git:

```bash
  $ git init
  ```

Create your biography file ```me.txt``` using ```nano``` or another text editor. Once in place, add and commit it to the repository:

  ```bash
$ git add me.txt
$ git commit -m "Add biography file"
  ```

Modify the file as described (modify one line, add a fourth line). To display the differences between its updated state and its original state, use ```git diff```:

  ```bash
$ git diff me.txt
  ```
  
 [Episode 5 image 1](episode5_img1.md)

