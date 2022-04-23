# Lab Report 2

Hello! Welcome to Lab Report 2. This report will show the process of debugging a file with different test cases.

## Test 1. File Link in the Middle 
---
Here is the [link](https://github.com/gmantuhac/markdown-parser/blob/main/test-fileinmiddle.md) to the file that causes an error when ran.

![Symptom1](https://cdn.discordapp.com/attachments/938667785679147030/967376340498124820/unknown.png)
*Picture 1a:* Symptom of [file](https://github.com/gmantuhac/markdown-parser/blob/main/test-fileinmiddle.md) 

![Fix1](https://cdn.discordapp.com/attachments/938667785679147030/967376650616569856/unknown.png)
*Picture 1b:* The fix needed for the file to run

Since the file is in the middle, there are extra spaces after the link which would mean that the file would keep looking for an open bracket thus causing an infinite loop. Because of the infinite loop, java runs out of memory as seen in the picture. (**Picture 1a**).

## Test2. File With Only Brackets
---
Here is the second [link](https://github.com/gmantuhac/markdown-parser/blob/main/test-onlybrackets.md) that causes an error when ran.

![Symptom2](https://cdn.discordapp.com/attachments/938667785679147030/967381201105084416/unknown.png)
*Picture 2a:* Symptomn of [file](https://github.com/gmantuhac/markdown-parser/blob/main/test-onlybrackets.md)

![Fix1](https://cdn.discordapp.com/attachments/938667785679147030/967380644067942441/unknown.png)
*Picture 2b:* The fix needed for file to run.

Because there are no parenthesis, the loop will keep ongoing until it finds the open parentheses, although it will never find it. Because of this, indexOf returns -1 as an actual index which, as seen in **Picture 2a**, will cause the symptom to have an index error.
