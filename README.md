# Linux-Fundamentals-Part-2
A walkthrough of my learning on TryHackMe in the second of three rooms dedicated to learning the Linux OS. (https://tryhackme.com/r/room/linuxfundamentalspart2)

<h2>Description</h2>
In this walkthrough room the new skills introduced include adding flags and arguments to commands, more filesystem commands for copying and moving files and directories, how to assign permissions in the discretionary access control scheme, and running scripts and executables.

<h2>Utilities Used</h2>

- <b>Terminal</b> 

<h2>Environments Used </h2>

- <b>Linux Ubuntu</b>

<h2>Project walk-through:</h2>

- <b>Accessing Your Linux Machine using SSH</b>
<p>In the previous room, Linux fundamentals 1, the attached machine was a simple terminal interface. In this second part of the Linux fundamentals series I learned how to use secure shell (SSH) to remotely access a Linux system.</p>
<br>
<p align="center">I used the command syntax ssh username@ip_address to login to secure shell with the username tryhackme and the matching password tryhackme.<br/>
  <img src="https://github.com/user-attachments/assets/c3c184df-46b8-4d66-bc87-8e54dc7d4f47" height="80%" width="80%" alt="image one"/>
</p>
<br />
<br />
- <b>Introduction to Flags and Switches</b>
<p>I learned that most linux commands accept arguments that you provide with a hyphen followed by a flag or a switch.</p>
<br>
<p align="center">To answer the questions in this section I pulled up the manual page for the list command using man ls. From there I was able to find that the flag to display the output in a "human readable" way is -h. <br/>
  <img src="https://github.com/user-attachments/assets/8dcae23f-95bf-40b8-8fa9-2b35a9084dc4" height="80%" width="80%" alt="image one"/>
</p>
- <b>Filesystem Interaction Continued</b>
<p>Building upon the commnads I learned in part one, which were ls, find, and cd, in this section I learned how to create, move, and delete files and folders using the command line.</p>
<br>
<p align="center">I created a new file called "newnote" with the touch command, then listed the contents of the working directory to confirm its creation. Then I used the file command to find out what file type "unknown1" is. Next, I moved "myfile" into "myfolder" using the mv command, and changed directory to myfolder to list its contents and find myfile there. Finally, I concatenated the contents of "myfile" to find the flag.<br/>
  <img src="https://github.com/user-attachments/assets/d5c65449-af65-40a5-a156-65fa3b258a56" height="80%" width="80%" alt="image one"/>
</p>
- <b>Permissions 101</b>
<p>Next I learned about user permissions and how to switch users.</p>
<br>
<p align="center">To discover who the owner of the file "important" is I used the list command with the flag -lh to see the file permissions and the owner. Once I discovered that the owner of the file is user2, I used the switch user command (su) to change from the tryhackme user to the user2 user. Then, being logged in as user2, I was able to concatenate (cat) the contents of "important" to find the flag.<br/>
  <img src="https://github.com/user-attachments/assets/c59e92ff-9d2c-4e69-b196-ebb302480a18" height="80%" width="80%" alt="image one"/>
</p>
- <b>Common Directories</b>
<p>In this last section of part two I learned about four common directories in Linux: /etc, /var, /root, and /tmp.</p>
<br>
<p align="center">I read the descriptions of the etc, var, root, and tmp directories and used that information to answer the questions below.<br/>
  <img src="https://github.com/user-attachments/assets/22240b2b-8604-430e-947d-32626669b02a" height="80%" width="80%" alt="image one"/>
</p>
