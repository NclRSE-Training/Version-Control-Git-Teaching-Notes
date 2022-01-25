
## 4.4 ```bio``` Repository

- Create a new Git repository on your computer called ```bio```.
- Write a three-line biography for yourself in a file called ```me.txt```, commit your changes
- Modify one line, add a fourth line
- Display the differences between its updated state and its original state.

<details>
  <summary>
Solution
  </summary>

If needed, move out of the <code>recipes</code> folder:

  <pre><code>$ cd ..</code></pre>

  Create a new folder called <code>bio</code> and ‘move’ into it:

  <pre><code>$ mkdir bio
$ cd bio</code></pre>

Initialise git:

  <pre><code>$ git init</code></pre>

  Create your biography file <code>me.txt</code> using <code>nano</code> or another text editor. Once in place, add and commit it to the repository:

  <pre><code>$ git add me.txt
$ git commit -m "Add biography file"</code></pre>

Modify the file as described (modify one line, add a fourth line). To display the differences between its updated state and its original state, use <code>git diff</code>:

  <pre><code>$ git diff me.txt</code></pre>
  
</details>
  
[Episode 5 image 1](episode5_img1.md)
