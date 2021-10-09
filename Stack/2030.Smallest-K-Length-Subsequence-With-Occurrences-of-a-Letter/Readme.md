### 2030.Smallest-K-Length-Subsequence-With-Occurrences-of-a-Letter

本题本质和```402.Remove-K-Digits```差不多。只不过多在单调栈的维护递增序列的过程中需要注意两个条件：1. 删除的字符总数不能超过k0，即```s.size()-k```；并且删除的letter数目不能超过k1，即letter出现的总频次减去repetition. 

我们用单调栈构建了一个递增序列之后，可能它的长度太长，即删减的字符不够多。此时我们必须继续从尾部开始删字符。删除尾部的操作同样延续之前的两个条件：1. 删除的字符总数不能超过k0；2. 删除的letter数目不能超过k1。如果不能删除，就保留该字符，处理下一个。