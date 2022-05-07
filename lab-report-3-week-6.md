# Lab Report 3
Hello! Welcome to Lab Report 3! This lab will mainly show the group tests that were covered in Lab 5.

## Streamlining `ssh` Configuration
---
![Image1a](https://cdn.discordapp.com/attachments/938667785679147030/972281522751176834/unknown.png)
*Image 1a:* Creating config file

To create the config file, I needed to first change the directory into my .ssh from my home directory. Then I creatd a txt file that had the contents to streamline my logging in process for my ieng6 account. Then I copied the contents into an actual config file.

![Image2a](https://cdn.discordapp.com/attachments/938667785679147030/972281971097108520/unknown.png)
*Image 2a:* Logging in with alias

With the config file, I am able to log in with the new alias I chose. Only uses `
`ssh ieng6`

![Image3a](https://cdn.discordapp.com/attachments/938667785679147030/972286295818764358/unknown.png)
*Image 3a:* Using `scp` with alias

Here, I used `scp` to copy a file into my `ieng6` account with the new alias. This streamlines the whole process much easier.

## Setup GitHub Access from `ieng6`
---
![Image1b](https://cdn.discordapp.com/attachments/938667785679147030/972288393088208938/unknown.png)
*Image 1b:* GitHub key

Here is where I stored my key from my GitHub Account. 

![Image2b](https://cdn.discordapp.com/attachments/938667785679147030/972288957264060416/unknown.png)
*Image 2b*: Key in personal computer

Here is where the key is stored within my personal computer.
![Image3-b](https://cdn.discordapp.com/attachments/938667785679147030/972294015569510420/unknown.png)
![Image4-b](https://cdn.discordapp.com/attachments/938667785679147030/972294538779570246/unknown.png)
![Image5-b](https://cdn.discordapp.com/attachments/938667785679147030/972293352177401866/unknown.png)
*Images 3b, 4b, 5b*: The long process using `git` commands

Here is a couple images showing my process for comitting and pushing a change onto GitHub. I included most of the process since it shows my learning process through the process. (Even though it was a bit frustrating).

Here is the new [file](https://github.com/gmantuhac/markdown-parser/blob/main/testfile.txt) I was able to commit as a result of this process

## Group 3
---
![Image1c](https://cdn.discordapp.com/attachments/601574874007207937/972398905662791701/unknown.png)
*Image 1c*: Directory onto `ieng6`

Here, I am able to copy my entire directory onto my `ieng6` account. In addition, this command uses my alias to further streamline the process.
![Image2c](https://cdn.discordapp.com/attachments/938667785679147030/972401577375694888/unknown.png)
*Image 2c*: Running the tests

With the directory copied in my `ieng6` account, I am able to run the tests within the directory, which pass.

![Image3-c](https://cdn.discordapp.com/attachments/938667785679147030/972403365977927690/unknown.png)
![Image4-c](https://cdn.discordapp.com/attachments/938667785679147030/972403844522856468/unknown.png)
*Images 3c and 4c*: Using `;` to combine commands

By using `;`, I am able to combine the `scp` command and the `ssh` command to copy the directory and log into my account in one-go. From there, I ran the tests again to make sure they pass and work. This makes the process quicker.