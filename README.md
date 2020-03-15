
## 项目背景 BackGround

直播后台消息通道敏感词过滤

## Description

Aho-Corasick is a multiple string matching algorithm.

I implement the algorithm in trie.go

In filter.go, I use the built trie to search sensitive words,and filter them out.

In test1.go, I test the filter function.

In test2.go, I implement a simple http server, and the dictionary can be asynchronously hot-updated and hot-reloaded using command: 'kill -1 pid'.

go run test1.go
go run test2.go

I tested for a dictionary file which contains 140W lines of diffrent sensitive phrases and 2100W charactors and totally 35M in size. It takes 50s to build the according trie, and it takes 1.5s to filter the all phrases out from a given text file which is the same to the dictionary file ( the worst case ) in a routine. And the total memory usage of the process is 2.4G.

For further optimization, you can allocate larger memory every time to avoid memory fragmentation.

For more details, please refer to book named "Flexible Pattern Matching Strings".

## Citation

Cited by : [Cyber Security and Foundations of Cryptography](https://github.com/11061055/php-7.3.0-ext-curl/wiki/0.-%E7%BD%91%E7%BB%9C_____%E5%AF%86%E7%A0%81%E5%AD%A6%E4%B8%8E%E7%BD%91%E7%BB%9C%E5%AE%89%E5%85%A8)
