# Lecture 5: Shell Scripting
##

### Overview
This lecture focused heavily on practicing BASH scripting skills in order to complete a tangible task; handling COVID data.  

### **Scripting 'covid.sh':**  
In the last lecture, we worked on a shell script called 'covid.sh'.  
The purpose of our 'covid.sh' script is to collect COVID data from the New York Times,  
and represent it using our shell.

The following code is what we have so far:  
```  
#!/bin/bash

# make a temp file to store the covid data
temp_file=$(mktemp)

# download the latest NYT covid data and store it to our temp file
curl -s -k -o $temp_file https://raw.githubusercontent.com/nytimes/covid-19-data/master/us-states.csv

# print the covid data to the shell
less $temp_file 

#clean up the temporary file
rm $temp_file
```