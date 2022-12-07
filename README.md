# Pig-0.17.0

Pig WordCount Commands

```
input = LOAD '/path/to/file/' AS(line:Chararray);
Words = FOREACH input GENERATE FLATTEN(TOKENIZE(line,' ')) AS word;
Grouped = GROUP words BY word;
wordcount = FOREACH Grouped GENERATE group, COUNT(words); 
```
