Write a script that prints the absolute path name of the current working directory.
(#!/bin/bash
# Get the absolute path of the current working directory
current_dir="$(pwd)"
# Print the absolute path
echo "Current working directory: $current_dir")

Display the contents list of your current directory.
(#!/bin/bash
# List the contents of the current directory
ls)

Write a script that changes the working directory to the user’s home directory.
(#!/bin/bash
# Change the working directory to the user's home directory
cd ~
# Print the new working directory
echo "Changed working directory to: $PWD")

Display current directory contents in a long format
(#!/bin/bash
# List the contents of the current directory in long format
ls -l )

Display current directory contents, including hidden files (starting with .). Use the long format.
(#!/bin/bash
# List the contents of the current directory, including hidden files, in long format
ls -la )

Create a script that creates a directory named my_first_directory in the /tmp/ directory.
(#!/bin/bash
mkdir -p /tmp/my_first_directory) 
-p: the -p option with the mkdir command to create both the target directory and any necessary parent directories.

Move the file betty from /tmp/ to /tmp/my_first_directory.
(#!/bin/bash
mv /tmp/betty /tmp/my_first_directory/ )

Delete the file betty.
(#!/bin/bash
rm /tmp/my_first_directory/betty )

Delete the directory my_first_directory that is in the /tmp directory.
(#!/bin/bash
rm -r /tmp/my_first_directory )

Write a script that changes the working directory to the previous one.
(#!/bin/bash
# Change the working directory to the previous one
cd -
# Print the new working directory
echo "Changed working directory back to: $PWD" )

Write a script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the /boot directory (in this order), in long format.
(#!/bin/bash
ls -la . .. /boot )

Write a script that prints the type of the file named iamafile. The file iamafile will be in the /tmp directory when we will run your script.
(#!/bin/bash
file -b /tmp/iamafile ) 
-b: the -b option to display the file type in a brief format.

Create a symbolic link to /bin/ls, named __ls__. The symbolic link should be created in the current working directory.
(#!/bin/bash
ln -s /bin/ls __ls__ ) 
ln: The ln command is used to create links.
-s: The -s option specifies that we are creating a symbolic link.

Create a script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.
(#!/bin/bash

cp -u .*.html ..
)
-u: The -u option ensures that only newer files are copied.

Create a script that moves all files beginning with an uppercase letter to the directory /tmp/u.
(#!/bin/bash
mv [[:upper:]]* /tmp/u/
)
Create a script that deletes all files in the current working directory that end with the character ~.
(#!/bin/bash
rm -f *~
)
-f: The -f option stands for "force" and allows the removal of files without confirmation.

Create a script that creates the directories welcome/, welcome/to/ and welcome/to/school in the current directory.
(#!/bin/bash
mkdir -p welcome/to/school
)
mkdir -p: The -p option allows you to create parent directories if they do not exist.

Write a command that lists all the files and directories of the current directory, separated by commas (,).
(#!/bin/bash
ls -amvp )
-a: List all entries, including hidden files and directories (those starting with a dot).
-m: List the entries in a comma-separated format.
-v: Sort the entries naturally (as opposed to lexicographically).
-p: Append a slash (/) to directory names to easily distinguish them.

Create a magic file school.mgc that can be used with the command file to detect School data files. School data files always contain the string SCHOOL at offset 0.
(Created a plain text file named school.mgc using vim
Added the following content to the school.mgc file:
0       string  SCHOOL  School data file
This line specifies that it should look for the string "SCHOOL" at offset 0 and provide the description "School data file" when it matches.
Saved the school.mgc file.
Then, I used the file command with my custom magic file to detect School data files:
file -m school.mgc )
