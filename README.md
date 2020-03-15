
## BackGround

Sensitive words filtering.

## Description

```
Aho-Corasick is a multiple string matching algorithm.

In trie.go,     I implement the algorithm in trie.go

In filter.go,   I use the built trie to search sensitive words,and filter them out.

In test1.go,    I test the filter function.

In test2.go,    I implement a simple http server, and the dictionary can be asynchronously 

                hot-updated and hot-reloaded using command: 'kill -1 pid'.
```
```
go run test1.go
go run test2.go
```
```
I tested for a dictionary file which contains 140W lines of diffrent sensitive phrases

and 2100W charactors and totally 35M in size. It takes 50s to build the according trie,

and it takes 1.5s to filter the all phrases out from a given text file which is the same

to the dictionary file (worst case) in a routine. The total memory of the process is 2.4G.

Further optimization, you can allocate large memory each time to avoid memory fragmentation.

For more details, please refer to book named "Flexible Pattern Matching Strings".
```

## Citation

Refer to : [Flexible Pattern Matching Strings](https://www.cambridge.org/core/books/flexible-pattern-matching-in-strings/D610D1F9C4744A864D73904B24EF602B)

Cited by : [Cyber Security and Foundations of Cryptography](https://github.com/11061055/php-7.3.0-ext-curl/wiki/0.-%E7%BD%91%E7%BB%9C_____%E5%AF%86%E7%A0%81%E5%AD%A6%E4%B8%8E%E7%BD%91%E7%BB%9C%E5%AE%89%E5%85%A8)
