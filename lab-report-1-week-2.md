# Lab Report 1

Hello! Welcome to Lab Report 1. This report will be based for *Windows* users. 

## Step 1. Installing VSCode
___

Visit the [VSCode](https://code.visualstudio.com/) website and click the blue button saying **Download for Windows**. Once VSCode has downloaded, open VSCode up and a window displaying the software should open up.
![DownloadVSCode](https://cdn.discordapp.com/attachments/938667785679147030/962614294850203648/unknown.png)

## Step 2. Remotely Connecting
___

First we need to look up our [account](https://sdacs.ucsd.edu/~icc/index.php) for CSE15L. If this is your first time logging into your account, just say yes to the prompt the terminal gives and input your password (Password shoudl look invisible since the system is very secure). Your terminal should look something similar to this:
![RemoteConnect](https://cdn.discordapp.com/attachments/938667785679147030/962624424568307782/unknown.png)

## Step 3. Running Commands
___

We will now run some commands on both your computer and the computer we have ssh'd in. Some of these commands are:

* `cd ~`
* `cd`
* `ls`
* `ls -lat`
* `ls -a`

Try these on your own and see how it compares between the two terminals.
![CommandEx](https://cdn.discordapp.com/attachments/938667785679147030/962629032497790986/unknown.png)

## Step 4. Moving Files w/ `scp`
___

Create a file called `test.java` and copy and paste the code bellow:

```
class WhereAmI {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}
```
On your main computer, type the following code; this will transfer the files between the two computers.

`scp test.java cs15lsp22zz@ieng6.ucsd.edu:~/`

Use `ls` to see the file in the ssh computer; compile and run the file on both terminals to make sure `test.java` is correct and transferred properly.

![scpEX](https://cdn.discordapp.com/attachments/938667785679147030/962634508149063710/unknown.png)

## Step 5. Setting an SSH key
___

To reduce the frustration when trying to transfer files and putting in our password, we use ssh keys. Use the code below in your terminal:
```
$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/<user-name>/.ssh/id_rsa): /Users/<user-name>/.ssh/id_rsa
Enter passphrase (empty for no passphrase): 
```

![sshKeyCreation](https://cdn.discordapp.com/attachments/938667785679147030/962638125920845834/unknown.png)

(Extra [steps](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_keymanagement#user-key-generation) for Windows users)

![WindowsSteps](https://cdn.discordapp.com/attachments/938667785679147030/962642002145583134/unknown.png)

After all this, follow the code below to copy the public key (`id_rsa.pub`) onto the `ssh` directory. 

## Step 6. Optimizing Remote Running
___

With the use of our ssh key, we're now able to run comands from our pc to the remote server directly. This can be done using the command with quotes at the end.

For example:

`$ ssh cs15lsp22zz@ieng6.ucsd.edu "ls"`

![optimizedRun](https://media.discordapp.net/attachments/938667785679147030/962649199822921738/unknown.png?width=1440&height=286)

## **END**