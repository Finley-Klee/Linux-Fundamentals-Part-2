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
  <img src="https://github.com/user-attachments/assets/c3c184df-46b8-4d66-bc87-8e54dc7d4f47" width="80%" alt="linux command line showing the ssh command connecting in the output"/>
</p>
<br />
<br />
- <b>Introduction to Flags and Switches</b>
<p>I learned that most linux commands accept arguments that you provide with a hyphen followed by a flag or a switch.</p>
<br>
<p align="center">To answer the questions in this section I pulled up the manual page for the list command using man ls. From there I was able to find that the flag to display the output in a "human readable" way is -h. <br/>
  <img src="https://github.com/user-attachments/assets/8dcae23f-95bf-40b8-8fa9-2b35a9084dc4" width="80%" alt="the manual page fromt the ls command with the -h flag line highlighted"/>
</p>
- <b>Filesystem Interaction Continued</b>
<p>Building upon the commnads I learned in part one, which were ls, find, and cd, in this section I learned how to create, move, and delete files and folders using the command line.</p>
<br>
<p align="center">I created a new file called "newnote" with the touch command, then listed the contents of the working directory to confirm its creation. Then I used the file command to find out what file type "unknown1" is. Next, I moved "myfile" into "myfolder" using the mv command, and changed directory to myfolder to list its contents and find myfile there. Finally, I concatenated the contents of "myfile" to find the flag.<br/>
  <img src="https://github.com/user-attachments/assets/d5c65449-af65-40a5-a156-65fa3b258a56" width="80%" alt="linux command line. Line one reads touch newnote, line two reads ls, line 3 reads important myfile myfolder unknown1, line 4 reads file unknown1, line 5 reads unknown1: ASCII text, line 6 reads mv myfile myfolder, line 7 reads cd myfolder, line 8 reads ls, line 9 reads myfile, line 10 reads cat myfile, line 11 reads THM{FILESYSTEM}."/>
</p>
- <b>Permissions 101</b>
<p>Next I learned about user permissions and how to switch users.</p>
<br>
<p align="center">To discover who the owner of the file "important" is I used the list command with the flag -lh to see the file permissions and the owner. Once I discovered that the owner of the file is user2, I used the switch user command (su) to change from the tryhackme user to the user2 user. Then, being logged in as user2, I was able to concatenate (cat) the contents of "important" to find the flag.<br/>
  <img src="https://github.com/user-attachments/assets/c59e92ff-9d2c-4e69-b196-ebb302480a18" width="80%" alt="the first line of the command line reads ls -lh, followed by the output of the files and directories in a table format with the file permissions in the leftmost column, then moving right the owner username, another column next to that repeats that username, then the date the file was last modified in the next column, followed by the name in the rightmost column. The next line reads su user2, then password: and a blank after that because the password is not printed, then the next line reads cat important and the last line reads THM{SU_USER2}."/>
</p>
- <b>Common Directories</b>
<p>In this last section of part two I learned about four common directories in Linux: /etc, /var, /root, and /tmp.</p>
<br>
<p align="center">I read the descriptions of the etc, var, root, and tmp directories and used that information to answer the questions below.<br/>
  <img src="https://github.com/user-attachments/assets/22240b2b-8604-430e-947d-32626669b02a" width="80%" alt="a white background with questions over gray background rounded rectangular boxes with answers to the left of rounded rectangular bright green boxes that have a check mark and correct answer written on them. The first question reads what is the directory path that we would expect logs to be stored in and the answer reads /var/log/, the second question reads What root directory is similar to how RAM on a computer works, and the answer reads /tmp, the last question reads name the home direcotry of the root user, and the answer reads /root."/>
</p>
