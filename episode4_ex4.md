
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

  <pre>
$ cd ..
  </pre>

Create a new folder called ```bio``` and ‘move’ into it:

  <pre>
$ mkdir bio
$ cd bio
  </pre>

Initialise git:

  <pre>
  $ git init
  </pre>

Create your biography file ```me.txt``` using ```nano``` or another text editor. Once in place, add and commit it to the repository:

  <pre>
$ git add me.txt
$ git commit -m "Add biography file"
  </pre>

Modify the file as described (modify one line, add a fourth line). To display the differences between its updated state and its original state, use <code>git diff</code>:

  <pre>
$ git diff me.txt
  </pre>
  
  </details>
  
 [Episode 5 image 1](episode5_img1.md)

