### Pig-0.17.0

Pig WordCount Commands

```
lines = LOAD '/path/to/file/' AS(line:Chararray);
words = foreach lines GENERATE FLATTEN(TOKENIZE(line)) as word;
grouped = GROUP words by word;
wordcount = foreach grouped GENERATE group . COUNT(words); 
```
