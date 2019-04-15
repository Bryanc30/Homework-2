**Hoffman2**

To log on to Hoffman2, I do the following:

1. Type in "Chrome:Apps" on my chrome browser

2. Select "Secure Shell App"

3. On the connection line, type "[c177-06@hoffman2.idre.ucla.edu](mailto:c177-06@hoffman2.idre.ucla.edu)"

4. For username, use "c177-06", and for the address use “hoffman2.idre.ucla.edu”

5. Then, click the connect button at the bottom right

6. When prompted, I type my password

Once I login, I type "qrsh" to request a compute node to perform my work on, rather than the login node that I started at.

**Using ls**

When using the -l flag, you bring up a list of directory contents in a long listing format. When using both the -l and the -h flag, you bring up a list of directory contents in a long listing format, in print sizes that are in a human-readable format.

When using ls -R -t, you bring up a list of directory contents that lists the subdirectories recursively, in order of which was most recently modified.

**Shortcuts**

1. "~" is your home directory

2. "../" is one directory up from where you currently are

3. "./" refers to your current directory

    1. $ cd . Goes to current directory

    2. $ cd / Goes to root directory

    3. $ cd /home/amanda Goes to nothing, since this directory doesn’t exist

    4. $ cd ../.. This goes up two directories to the users directory

    5. $ cd ~ This brings her to the home directory

    6. $ cd home Does nothing, since there is no directory actually called "home"

    7. $ cd ~/data/.. This brings her to the home directory

    8. $ cd This brings her to the home directory with even less text

    9. $ cd .. This goes up one directory, which would then be her home directory

        1. Amanda could use commands (e), (g), (h), and (i) to go to her home directory. 

**File systems**

1.

a. ../backup: No such file or directory

b. 2012-12-01 2013-01-08 2013-01-27

c. 2012-12-01/ 2013-01-08/ 2013-01-27/

d. original/ pnas_final/ pnas_sub/

Option (D) will be displayed, since the command inputted is referring to the path /Users/backup/

2.

a. ls pwd

b. ls -r -F

c. ls -r -F /Users/backup

pnas_sub/ pnas_final/ original/

Commands (b) and (c)  will result in this output.

**Making files and appending stuff**

    1. The touch command creates the file my_file.txt in the directory you’re currently in. Yes, you can see the new file in the GUI file explorer.

    2. Using ls -l to inspect the files, my_file.txt is 0 bytes, since it is empty.

    3. You might want to create a file this way if something you’re doing requires an empty file as that action’s destination.

    4. Using touch will not allow you to edit my_file.txt, I believe it only refreshes the activity on said file to prevent it from being forgotten somehow or accidentally deleted

1.  

    5. The > operator causes the string "hello" to be written in the text file testfile01.txt, but every time we use this command, the file is entirely overwritten. If we use >> instead, however, the edit is appended to what already exists in the file. 

2. Option (c) would correspond to the file animals-subset.txt.

**Copying, Moving and deleting files**

1. Filled in blanks: $ mv ...analyzed/sucrose.dat ../analyzed/maltose.dat .

2. You should use command (b). 

3. (b) "recombine" is the output of the closing ls command.

4. Including the -i will make it so you are asked if you really want to delete the file. This is helpful because there is no way of recovering deleted files in this shell system.

5. It will copy the two files to that directory.

6. It will give you an error message because you have not given it a directory to copy the files to.

        1. cp *calibration.txt backup/calibration

        2. cp 1025-11-* send_to_bob/all_november_files/

        3. cp *-23dataset* send_to_bob/all_datasets_created_on_a_23rd/

        4. She should run the command "mv *.dat analyzed"

7. The first and second command sets would achieve this objective. The third command set would leave you with an error message since mkdir does not create subdirectories without first having a directory. They must be created one at a time. The last command set would create both the processed and raw directories at the same "level" as the data directory.

**Sort, Piping, Uniq, Cut**

1. -n causes sort to sort by numerical order.

2. "c -1 * | sort - n | head -n 3" (option 4) would work.

3. Uniq only removes adjacent duplicated lines because in very large data sets, it is likely that two lines will be the same, but unlikely that those two lines would be adjacent to one another. Another command you could combine with it in a pipe to remove all duplicated lines is " sort salmon.txt | uniq"

4. The text that passes through each of the pipes and the final redirect in the pipeline below is: 

    1. 2012-11-06,rabbit

    2. 2012-11-06,deer

    3. 2012-11-05,raccoon

5. You could also use this command:

        1. cut -d , -f 2 animals.txt | sort | uniq

6. You would use this command: 

        2. cut -d , -f 2 animals.txt | sort | uniq -c

**Wildcards**

        1. You can match the same set of files with these basic wildcard expressions:

            1. ls *A.txt

            2. ls *B.txt

        2. The small difference between the outputs is that they are separated, since you put in two separate commands.

        3. The new expression would produce an error message if there are no files with an ending of A.txt or B.txt.

1. You would use the second command, rm *.txt

