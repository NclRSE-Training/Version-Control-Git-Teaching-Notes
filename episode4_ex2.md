
## 4.2 Committing Changes to Git

Which command(s) below would save the changes of ```myfile.txt``` to my local Git repository?

<ol>
  <li>
    <pre><code>$ git commit -m "my recent changes"</code></pre>
  </li>
  <li>
    <pre><code>$ git init myfile.txt
$ git commit -m "my recent changes"</code></pre>
  </li>
  <li>
    <pre><code>$ git add myfile.txt
$ git commit -m "my recent changes"</code></pre>
  </li>
  <li>
    <pre><code>$ git commit -m myfile.txt "my recent changes"</code></pre>
  </li>
</ol>

<details>
  <summary>
    Solution
  </summary>
  
  <ol>
    <li>Would only create a commit if files have already been staged.</li>
    <li>Would try to create a new repository.</li>
    <li>Is correct: first add the file to the staging area, then commit.</li>
    <li>Would try to commit a file “my recent changes” with the message <code>myfile.txt</code>.</li>
  </ol>
  
  </details>

[Episode 4 exercise 3](episode4_ex3.md)
