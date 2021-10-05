
## 6.1 Ignoring Nested Files

Given a directory structure that looks like:

```console
receipts/data
receipts/plots
```

How would you ignore only ```receipts/plots``` and not ```receipts/data```?

<details>
<summary>Solution</summary>

If you only want to ignore the contents of ```receipts/plots```, you can change your ```.gitignore``` to ignore only the ```/plots/``` subfolder by adding the following line to your .gitignore:

```console
receipts/plots/
```

This line will ensure only the contents of ```receipts/plots``` is ignored, and not the contents of ```receipts/data```.

As with most programming issues, there are a few alternative ways that one may ensure this ignore rule is followed. The “Ignoring Nested Files: Variation” exercise has a slightly different directory structure that presents an alternative solution. Further, the discussion page has more detail on ignore rules.

</details>
  
[Episode 6 exercise 2](episode6_ex2.md)
