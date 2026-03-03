# 🐧 Linux and Bash Command Cheat Sheet

This repository contains basic Linux and Bash commands.
Good for beginners in System Administration, Cybersecurity, DevOps, and IT Support.

---

## Getting Information

```bash
# return your user name
whoami

# return your user and group id
id

# return operating system name and details
uname -a

# display manual for a command
man top

# get help for a command
curl --help

# show current date and time
date
```

---

## Monitoring Performance and Status

```bash
# list running processes
ps

# list all running processes
ps -e

# show CPU and memory usage
top

# show disk usage
df
```

---

## Working with Files

```bash
# copy file
cp file.txt new_path/new_name.txt

# rename or move file
mv this_file.txt that_path/that_file.txt

# delete file (verbose)
rm this_old_file.txt -v

# create empty file or update timestamp
touch a_new_file.txt

# make file executable
chmod +x my_script.sh

# count lines
wc -l table_of_data.csv

# count words
wc -w my_essay.txt

# count characters
wc -m some_document.txt

# search word in files (case insensitive, whole word)
grep -iw hello *.txt

# show file names with matching word
grep -l hello *.txt
```

---

## Navigating Directories

```bash
# list files by date
ls -lrt

# find .sh files
find . -name "*.sh"

# show current directory
pwd

# create directory
mkdir new_folder

# go up one level
cd ../

# go to home
cd ~

# go to specific directory
cd another_directory

# remove empty directory
rmdir temp_directory -v
```

---

## Printing File and String Contents

```bash
# show file content
cat my_shell_script.sh

# show file page by page
more ReadMe.txt

# show first 10 lines
head -10 data_table.csv

# show last 10 lines
tail -10 data_table.csv

# print text
echo "I am not a robot"

# print variable
echo "I am $USERNAME"
```

---

## Compression and Archiving

```bash
# create tar archive
tar -cvf my_archive.tar file1 file2 file3

# create compressed tar.gz archive
tar -czvf my_archive.tar.gz file1 file2 file3

# zip files
zip my_zipped_files.zip file1 file2

# unzip file
unzip my_zipped_file.zip

# unzip to specific folder
unzip my_zipped_file.zip -d extract_directory
```

---

## Network Operations

```bash
# show hostname
hostname

# test internet connection
ping www.google.com

# show network interfaces
ifconfig
ip addr

# display website content
curl https://example.com

# download file
wget https://example.com/file.zip
```

---

## Bash Shebang

```bash
#!/bin/bash
```

---

## Pipes and Filters

```bash
# sort output reverse
ls | sort -r

# show first 20 lines of manual
man ls | head -20
```

---

## Shell and Environment Variables

```bash
# list shell variables
set

# create variable
my_planet=Earth

# show variable
echo $my_planet

# list environment variables
env

# export variable
export my_planet
export my_galaxy="Milky Way"
```

---

## Metacharacters

```bash
# comment
# this is a comment

# command separator
echo "files:"; ls

# wildcard
ls *.json

# single character wildcard
ls file_2021-06-??.json
```

---

## Quoting

```bash
# single quotes (literal)
echo 'My home directory: $HOME'

# double quotes (evaluate variable)
echo "My home directory is $HOME"

# escape special character
echo "This dollar sign: \$"
```

---

## I/O Redirection

```bash
# redirect output to file
echo "Write this text" > x

# append output
echo "Add this line" >> x

# redirect error
bad_command 2> error.log

# append error
bad_command 2>> error.log

# input redirection
tr "[a-z]" "[A-Z]" < a_text_file.txt

# same using pipe
cat a_text_file.txt | tr "[a-z]" "[A-Z]"
```

---

## Command Substitution

```bash
THE_PRESENT=$(date)
echo "There is no time like $THE_PRESENT"
```

---

## Command Line Arguments

```bash
./My_Bash_Script.sh arg1 arg2 arg3
```

---

## Sequential vs Parallel Execution

```bash
# sequential
start=$(date); ./MyBigScript.sh; end=$(date)

# parallel
./script1.sh & ./script2.sh
```

---

## Scheduling Jobs with Cron

```bash
# open crontab
crontab -e

# syntax
# m h dom mon dow command

# every Sunday at 6:15 PM
15 18 * * 0 date >> sundays.txt

# first minute of every month
1 0 1 * * ./My_Shell_Script.sh

# every Monday at 3 AM backup home directory
0 3 * * 1 tar -czvf my_backup.tar.gz $HOME

# list cron jobs
crontab -l
```
