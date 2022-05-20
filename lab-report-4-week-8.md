# Lab Report 4

Hello! Welcome to Lab Report 4. This lab report will show my test process for the lab in week 7.

Here is the link to my [repository](https://github.com/gmantuhac/markdown-parser) and here is the link to the [repository](https://github.com/Miyuki-L/markdown-parser) I reviewed in week 7.

Here are the code snippets I need to test.

### ***Snippet 1***
```
`[a link`](url.com)

[another link](`google.com)`

[`cod[e`](google.com)

[`code]`](ucsd.edu)
```
For snippet 1, I expect to have the outcome:

`[url.com, google.com, google.com, ucsd.edu]`

### ***Snippet 2***
```
[a [nested link](a.com)](b.com)

[a nested parenthesized url](a.com(()))

[some escaped \[ brackets \]](example.com)
```
For snippet 2, I expect to have the outcome:

`[a.com, a.com, example.com]`

### ***Snippet 3***
```
[this title text is really long and takes up more than 
one line

and has some line breaks](
    https://www.twitter.com
)

[this title text is really long and takes up more than 
one line](
https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule
)


[this link doesn't have a closing parenthesis](github.com

And there's still some more text after that.

[this link doesn't have a closing parenthesis for a while](https://cse.ucsd.edu/



)

And then there's more text
```
For snippet 3, I expect to have the outcome:

`[https://www.twitter.com, https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule, https://cse.ucsd.edu/]`

## My Code Outcome
---

From my code outcome, all tests failed. Here is their JUnit results:
![MyTests](https://cdn.discordapp.com/attachments/938667785679147030/977133620194058280/unknown.png)

## Reviewed Code Outcome
---

From the other code outcome, all tests failed. Here is their JUnit results:
![OtherTests](https://cdn.discordapp.com/attachments/938667785679147030/977135560370044928/unknown.png)

## Question Answers
---

**Q1**: Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.

**A1**: I believe that a small code change is possible for backticks. I believe that I could just include an if statement to detect any backtics and remove them from the returned array.

**Q2**: Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.

**A2**: From the result from my code, I believe that a small code change is possible for this test. To do so, you would probably need a for loop and if statements to get a link between an open parenthesis and a closed paenthesis. Then, if there is any nested characters (brackets or parenthesis), remove them from the returned array.

**Q3**: Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.

**A3**: I do not believe that you can make a small code change for snippet 3. This is because you would need to constantly entertain the possibility of extra spaces and lines in the final array which would take a good amount of code to remove. Also formatting the array to a proper organized order will also be a bit long when combining with what I mentioned previously. 




