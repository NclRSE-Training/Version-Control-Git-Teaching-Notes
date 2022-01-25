## 6.4 Ignoring all data Files in a Directory

Assuming you have an empty .gitignore file, and given a directory structure that looks like:

```console
receipts/data/market_position/gps/a.dat
receipts/data/market_position/gps/b.dat
receipts/data/market_position/gps/c.dat
receipts/data/market_position/gps/info.txt
receipts/plots
```

What’s the shortest ```.gitignore``` rule you could write to ignore all ```.dat``` files in ```result/data/market_position/gps```? Do not ignore the ```info.txt```.


<details>
  <summary>
    Solution
  </summary>

  <p>
    Appending <code>receipts/data/market_position/gps/*.dat</code> will match every file in <code>receipts/data/market_position/gps</code> that ends with <code>.dat</code>. The file <code>receipts/data/market_position/gps/info.txt</code> will not be ignored.
  </p>
      
</details>

[Episode 6 Exercise 5](episode6_ex5.md)
