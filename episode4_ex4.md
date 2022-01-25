## 4.4 ```bio``` Repository

- Create a new Git repository on your computer called ```bio```.
- Write a three-line biography for yourself in a file called ```me.txt```, commit your changes
- Modify one line, add a fourth line
- Display the differences between its updated state and its original state.

<details>
  <summary>
    Solution
  </summary>

  <p>
    If needed, move out of the <code>recipes</code> folder:
  </p>

  <pre><code>$ cd ..</code></pre>

  <p>
    Create a new folder called <code>bio</code> and ‘move’ into it:
  </p>

  <pre><code>$ mkdir bio
$ cd bio</code></pre>

  <p>
    Initialise git:
  </p>

  <pre><code>$ git init</code></pre>

  <p>
    Create your biography file <code>me.txt</code> using <code>nano</code> or another text editor. Once in place, add and commit it to the repository:
  </p>

  <pre><code>$ git add me.txt
$ git commit -m "Add biography file"</code></pre>

  <p>
    Modify the file as described (modify one line, add a fourth line). To display the differences between its updated state and its original state, use <code>git diff</code>:
  </p>

  <pre><code>$ git diff me.txt</code></pre>
  
</details>
  
[Episode 5 Image 1](episode5_img1.md)
