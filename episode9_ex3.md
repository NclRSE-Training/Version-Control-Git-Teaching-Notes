## 9.3 A Typical Work Session

You sit down at your computer to work on a shared project that is tracked in a remote Git repository. During your work session, you take the following actions, but not in this order:

* Make changes by appending the number ```100``` to a text file ```numbers.txt```
* Update remote repository to match the local repository
* Celebrate your success with beer(s)
* Update local repository to match the remote repository
* Stage changes to be committed
* Commit changes to the local repository

In what order should you perform these actions to minimize the chances of conflicts? Put the commands above in order in the action column of the table below. When you have the order right, see if you can write the corresponding commands in the command column. A few steps are populated to get you started.

order | action... | command...
:- | :- | :-
1 | |
2 | | ```echo 100 >> numbers.txt```
3 | |
4 | |
5 | |
6 | Celebrate! | ```AFK```

<details>
  <summary>
    Solution
  </summary>
  
  <table>
    <tr>
      <th>order</th>
      <th>action...</th>
      <th>command...</th>
    </tr>
    <tr>
      <td>1</td>
      <td>Update local</td>
      <td><code>git pull origin master</code></td>
    </tr>
    <tr>
      <td>2</td>
      <td>Make changes</td>
      <td><code>echo 100 >> numbers.txt</code></td>
    </tr>
    <tr>
      <td>3</td>
      <td>Stage changes</td>
      <td><code>git add numbers.txt</code></td>
    </tr>
    <tr>
      <td>4</td>
      <td>Commit changes</td>
      <td><code>git commit -m "Add 100 to numbers.txt"</code></td>
    </tr>
    <tr>
      <td>5</td>
      <td>Update remote</td>
      <td><code>git push origin master</code></td>
    </tr>
    <tr>
      <td>6</td>
      <td>Celebrate!</td>
      <td><code>AFK</code></td>
    </tr>
  </table>
</details>

[End]()
