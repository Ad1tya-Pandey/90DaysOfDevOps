# Task for day 5


## this is the shell script i used for completing the first two tasks combined

```
#!/bin/bash
dirname=$1

#for 2 arguments
if [ $# = 2 ]; then
numofdir=$2
#       for creating multiple directories
for ((i=1;i<=numofdir;i++)); do
        mkdir "$dirname$i"
done
#else if block for 3 arguments 
elif [ $# = 3 ]; then
startwith=$2
numofdir=$3
for ((i=startwith;i<=numofdir;i++)); do
        mkdir "$dirname$i"
done
#else condition for invalid parameters
else
  echo  "invalid arguments passed"


fi
```

## code for backup script
```
#!/bin/bash
       
     
# creating a backup directory with the current date 
backup_dir="backup-$(date +%Y%m%d)"
rm -rf $backup_dir
mkdir $backup_dir

#using copy command to copy all the commands from the current directory to the backup file
cp * $backup_dir

echo "Backup completed"

```
- to take regular backups of this directory we will add this script to the crontab in using the command
> crontab e
and as per our requirment we would append the file with a job which can be scheduled hourly , daily , weekly and so on 
here is the line which i added in the cronjob file in order to execute my backup file on hourly basis :
```
01 * * * * bash /home/kali/Desktop/shell-scripting/backup.sh
```
then had to use the command so that given job could take place form that very instance based upon the schedule 
> crontab l 


- used ```adduser username``` for adding users 
- to display the created users i viewd the contents of the ``` /etc/passwd/ ``` file and extracted only the username column using the awk command , the command was as follows:
> cat /etc/passwd | awk: '{print $1}'



<i> ps : i'm all set for upcoming days , this was fun !

