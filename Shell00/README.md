# 42Piscine :swimmer:

## Shell00

#### Ex00

This exercise asked to create a file called 'z', containing the letter 'Z'.

- I used the following command: vim z
- i (to enter insert mode)
- Z
- esc (to enter normal mode)
- :wq (to save and exit)

#### Ex01

This exercise asked to create a file, adjust the permissions, size and date and put it in a tar file.

I used following commands:

- touch testShell00
- truncate -s 40
- chmod 455 testShell00
- touch -t 06012342 testShell00
- tar -cf testShell00.tar testShell00

#### Ex02

The exercise asked to create several files, directories, hard and soft links, and change the permissions, size, dates. All files had to be put in a tar file.

- I created the files and directories with the touch and mkdir commands
- I created the hard link with the ln command and soft link with the -s flag
- I changed the size using the truncate -s command
- I changed the dates with the touch -t command, adding the -h flag for changing the date of the soft link
- I changed the permissions with chmod command
- I created the tar file with the tar -cf exo2.tar * command as requested

#### Ex03

The exercise asked to create an SSH key and submit the public key.

I used the following command:

	ssh-keygen -t rsa

and moved and changed the name of the public key file with the mv command.

#### Ex04

The exercise asked to put a command in a file called midLS, that would list the files and directories ordered by time, separated by commas and with a / after the directories.

I used following command:

	ls -tpm

#### Ex05

Asked to create a shell program that shows the hashes of the last 5 commits.

I created 6 empty commits with the following command:  
  
	git commit --allow-empty -m "test commit 1"

and looked up the flags needed to display only the 5 last hashes. (-5 --pretty="%H")

#### Ex06

Asked to create a program that would list untracked files in the current directory ignored by the .gitignore file, excluding files that are ignored by the standard ignore rules.

- I created a test file and put it in a .gitignore file to test the flags I looked up to select the files I wanted.

#### Ex07

We were given file a and the diff between a and an unknown file b. It asked to recreate file b.

- I copied a to b and applied the patch to file b.


#### Ex08

Asked to list and delete all files in the current directory and subdirectories that ended in '~', or started and ended in '#'.

- I created testfiles and directories ex. touch \\#test#
- I used the find command and looked up the flags and regular expressions needed to select the files and delete them.

#### Ex09

Task was to create a magic file that would detect files that have the string '42' at the 42nd byte.

- I used '41' as offset as we start counting at 0
- 'string' as the type of information that we're looking for
- '42' as the information we're looking to encounter
- a mesage to display
- testing was done with the following command:

	file -m ft_magic *

