
## 3.2 Correcting git init Mistakes

Jimmy explains to Alfredo how a nested repository is redundant and may cause confusion down the road. Alfredo would like to remove the nested repository. How can Alfredo undo his last git init in the cocktails subdirectory?

<details>
<summary>
  Solution – USE WITH CAUTION!
</summary>
        
### Background

Removing files from a git repository needs to be done with caution. To remove files from the working tree and not from your working directory, use

```bash
  $ rm filename
  ```

The file being removed has to be in sync with the branch head with no updates. If there are updates, the file can be removed by force by using the -f option. Similarly a directory can be removed from git using ```rm -r dirname``` or ```rm -rf dirname```.
 ### Solution

Git keeps all of its files in the ```.git``` directory. To recover from this little mistake, Alfredo can just remove the ```.git``` folder in the cocktails subdirectory by running the following command from inside the recipes directory:

```bash
  $ rm -rf cocktails/.git
  ```

But be careful! Running this command in the wrong directory, will remove the entire Git history of a project you might want to keep. Therefore, always check your current directory using the command ```pwd```.

</details>

[Episode 4](episode4.md)
