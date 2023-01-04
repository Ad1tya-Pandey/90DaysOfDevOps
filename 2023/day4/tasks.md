# task for day 4
- shell scripting is writting a list of commands in order to execute them in series by just running our script . this is a powerful tool since this will help us automate process as a  devops engineer which requires many commands usually but such scirpts would save our time
- "#!/bin/bash" is knows as shebang and it is return in the beginning of the bash file in order to let the system know that our file is a bash script , also we can use "#!/bin/sh" as shebang too since it specifies that our file is a shell script.
##Below is the bash script for required procedure:
#!/bin/bash</br>
echo "i will complete 90 days of devops challange"</br>
echo "------------------------------------------"
echo "Printing the first argument taken from user:" $1</br>
first_num=10</br>
second_num=2</br>
if [ first_num -gt second_num ]</br>
then</br>
echo "first num is greater"</br>
else</br>
echo "second num is greater"</br>
fi</br>
<i> ps : it was easy ! 

