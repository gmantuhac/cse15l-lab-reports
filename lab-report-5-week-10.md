# Lab Report 5

Hello! Welcome to my last lab report. Lab Report 5. This report will focus on testing different results using different versions of markdown parser.

When testing my results, I just opened two windows and tested each code side-by-side using the different versions of markdown parser.

**NOTE: IN THE SCREENSHOTS OF THE OUTPUTS, THE LEFT OUTPUT IS MY PERSONAL CODE WHILE THE RIGHT OUTPUT IS THE CODE PROVIDED IN LAB 9**

Here are the tests that I compared:

[Test 368](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/368.md?plain=1)

[Test 393](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/393.md?plain=1)

## Test 368
---
For the following test, here is the output from both code:

![Test 368](https://cdn.discordapp.com/attachments/938667785679147030/982141896715563018/unknown.png)

The correct output should be the left side (i.e. my implementation of the code).

In this test case, I believe that the implementation provided isn't able to continue copying the characters in the parenthesis. This is due to the fact that there are asterisks.

![Test 368 Solution](https://cdn.discordapp.com/attachments/938667785679147030/982146530729414666/unknown.png)

This section of code might be the issue in the implementation provided since it possibly just returns an empty string. To fix this, there needs to be some kind of code that just continues to add whatever's in the parenthesis.

## Test 393
---
For the following test, here is the output from both code:

![Test 393](https://cdn.discordapp.com/attachments/938667785679147030/982141464387657819/unknown.png)

Again I believe that the correct output is in the left side. While the code does not include the first part outside of the parenthesis, the point of markdown parser is to record links inside the parenthesis.

In this test case, like Test 368, the implementation is having trouble printing out the string because there are asterisks. This stops the code from putting the characters from the parenthesis into the brackets into the string.

![Test 393 Solution](https://cdn.discordapp.com/attachments/938667785679147030/982146530729414666/unknown.png)

I believe that the same section of code from Test 368 is the same issue. This is dealing with asterisks again and should be fixed by adding code to put all characters, including the asterisks into the string.



