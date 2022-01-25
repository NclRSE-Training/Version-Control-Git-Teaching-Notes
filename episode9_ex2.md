## 9.2 Conflicts on Non-textual files

What does Git do when there is a conflict in an image or some other non-textual file that is stored in version control?

<details>
  <summary>
    Solution
  </summary>

  <p>
    Let’s try it. Suppose Alfredo takes a picture of its guacamole and calls it <code>guacamole.jpg</code>.
  </p>
  <p>
    If you do not have an image file of guacamole available, you can create a dummy binary file like this:
  </p>

  <pre><code>$ head --bytes 1024 /dev/urandom > guacamole.jpg
$ ls -lh guacamole.jpg</code></pre>

  <pre><code>-rw-r--r-- 1 alflin 57095 1.0K Mar  8 20:24 guacamole.jpg</code></pre>

  <p>
    <code>ls</code> shows us that this created a 1-kilobyte file. It is full of random bytes read from the special file, <code>/dev/urandom</code>.
  </p>
  <p>
    Now, suppose Alfredo adds <code>guacamole.jpg</code> to his repository:
  </p>

  <pre><code>$ git add guacamole.jpg
$ git commit -m "Add picture of guacamole"</code></pre>

  <pre><code>[master 8e4115c] Add picture of guacamole
1 file changed, 0 insertions(+), 0 deletions(-)
create mode 100644 guacamole.jpg</code></pre>

  <p>
    Suppose that Jimmy has added a similar picture in the meantime. His is a picture of a guacamole with nachos, but it is also called <code>guacamole.jpg</code>. When Alfredo tries to push, he gets a familiar message:
  </p>

  <pre><code>$ git push origin master</code></pre>

  <pre><code>To https://github.com/alflin/recipes.git
! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/alflin/recipes.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.</code></pre>

  <p>
    We’ve learned that we must pull first and resolve any conflicts:
  </p>

  <pre><code>$ git pull origin master</code></pre>

  <p>
    When there is a conflict on an image or other binary file, git prints a message like this:
  </p>

  <pre><code>$ git pull origin master
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0)
Unpacking objects: 100% (3/3), done.
From https://github.com/alflin/recipes.git
* branch            master     -> FETCH_HEAD
6a67967..439dc8c  master     -> origin/master
warning: Cannot merge binary files: guacamole.jpg (HEAD vs. 439dc8c08869c342438f6dc4a2b615b05b93c76e)
Auto-merging guacamole.jpg
CONFLICT (add/add): Merge conflict in guacamole.jpg
Automatic merge failed; fix conflicts and then commit the result.</code></pre>

  <p>
    The conflict message here is mostly the same as it was for <code>guacamole.md</code>, but there is one key additional line:
  </p>

  <pre><code>warning: Cannot merge binary files: guacamole.jpg (HEAD vs. 439dc8c08869c342438f6dc4a2b615b05b93c76e)</code></pre>

  <p>
    Git cannot automatically insert conflict markers into an image as it does for text files. So, instead of editing the image file, we must check out the version we want to keep. Then we can add and commit this version.
  </p>
  <p>
    On the key line above, Git has conveniently given us commit identifiers for the two versions of <code>guacamole.jpg</code>. Our version is <code>HEAD</code>, and Jimmy’s version is <code>439dc8c0...</code>. If we want to use our version, we can use <code>git checkout</code>:
  </p>

  <pre><code>$ git checkout HEAD guacamole.jpg
$ git add guacamole.jpg
$ git commit -m "Use image of just guacamole instead of with nachos"</code></pre>

  <pre><code>[master 21032c3] Use image of just guacamole instead of with nachos</code></pre>

  <p>
    If instead we want to use Jimmy’s version, we can use <code>git checkout</code> with Jimmy’s commit identifier, <code>439dc8c0</code>:
  </p>

  <pre><code>$ git checkout 439dc8c0 guacamole.jpg
$ git add guacamole.jpg
$ git commit -m "Use image of guacamole with nachos instead of just guacamole"</code></pre>

  <pre><code>[master da21b34] Use image of guacamole with nachos instead of just guacamole</code></pre>

  <p>
    We can also keep both images. The catch is that we cannot keep them under the same name. But, we can check out each version in succession and rename it, then add the renamed versions. First, check out each image and rename it:
  </p>

  <pre><code>$ git checkout HEAD guacamole.jpg
$ git mv guacamole.jpg guacamole-only.jpg
$ git checkout 439dc8c0 guacamole.jpg
$ mv guacamole.jpg guacamole-nachos.jpg</code></pre>

  <p>
    Then, remove the old <code>guacamole.jpg</code> and add the two new files:
  </p>

  <pre><code>$ git rm guacamole.jpg
$ git add guacamole-only.jpg
$ git add guacamole-nachos.jpg
$ git commit -m "Use two images: just guacamole and with nachos"</code></pre>

  <pre><code>[master 94ae08c] Use two images: just guacamole and with nachos
2 files changed, 0 insertions(+), 0 deletions(-)
create mode 100644 guacamole-nachos.jpg
rename guacamole.jpg => guacamole-only.jpg (100%)</code></pre>

  <p>
    Now both images of guacamole are checked into the repository, and <code>guacamole.jpg</code> no longer exists.
  </p>

</details>

[Episode 9 Exercise 3](episode9_ex3.md)
