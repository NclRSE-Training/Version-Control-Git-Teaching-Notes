
## 6.3 Ignoring Nested Files: Variation

Given a directory structure that looks similar to the earlier Nested Files exercise, but with a slightly different directory structure:

```console
receipts/data
receipts/images
receipts/plots
receipts/analysis
```

How would you ignore all of the contents in the receipts folder, but not ```receipts/data```?

Hint: think a bit about how you created an exception with the ```!``` operator before.


<details>
  <summary>
  Solution
  </summary>

If you want to ignore the contents of ```receipts/``` but not those of ```receipts/data/```, you can change your ```.gitignor```e to ignore the contents of ```receipts``` folder, but create an exception for the contents of the ```receipts/data``` subfolder. Your ```.gitignore would``` look like this:

```console
receipts/*               # ignore everything in receipts folder
!receipts/data/          # do not ignore receipts/data/ contents
```

</details>

[Episode 6 exercise 4](episode6_ex4.md)
