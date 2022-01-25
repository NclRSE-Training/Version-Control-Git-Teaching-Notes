
## 3.2 Correcting git init Mistakes

Jimmy explains to Alfredo how a nested repository is redundant and may cause confusion down the road. Alfredo would like to remove the nested repository. How can Alfredo undo his last ```git init``` in the ```cocktails``` subdirectory?

<details>
  <summary>
Solution – USE WITH CAUTION!
  </summary>
        
  <h3>Background</h3>

Removing files from a git repository needs to be done with caution. To remove files from the working tree and not from your working directory, use

  <pre><code>$ rm filename</code></pre>

The file being removed has to be in sync with the branch head with no updates. If there are updates, the file can be removed by force by using the <code>-f</code> option. Similarly a directory can be removed from git using <code>rm -r dirname</code> or <code>rm -rf dirname</code>.
 
  <h3>Solution</h3>

  Git keeps all of its files in the <code>.git</code> directory. To recover from this little mistake, Alfredo can just remove the <code>.git</code> folder in the cocktails subdirectory by running the following command from inside the <code>recipes</code> directory:

  <pre><code>$ rm -rf cocktails/.git</code></pre>

But be careful! Running this command in the wrong directory, will remove the entire Git history of a project you might want to keep. Therefore, always check your current directory using the command <code>pwd</code>.

</details>

[Episode 4 image 1](episode4_img1.md)
