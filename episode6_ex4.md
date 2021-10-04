
## 6.4 Ignoring all data Files in a Directory

Assuming you have an empty .gitignore file, and given a directory structure that looks like:

```console
receipts/data/market_position/gps/a.dat
receipts/data/market_position/gps/b.dat
receipts/data/market_position/gps/c.dat
receipts/data/market_position/gps/info.txt
receipts/plots
```

What’s the shortest ```.gitignore``` rule you could write to ignore all ```.dat``` files in ```result/data/market_position/gps```? Do not ignore the info.txt.


<details>
  <summary>
Solution
  </summary>

Appending ```receipts/data/market_position/gps/*.dat``` will match every file in ```receipts/data/market_position/gps``` that ends with ```.dat```. The file ```receipts/data/market_position/gps/info.txt``` will not be ignored.

</details>

[Episode 6 exercise 5](episode6_ex5.md)
