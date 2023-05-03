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


**Using Command Line Arguments in BASH**  
Arguments come after the executable and are an array of strings.  
We refer to these arguments with indices $1, $2, ...$n.  
To combine these arguments, we can add quotation marks to make two string arguments into one; i.e.:  
`- { "New York" }` instead of `{"New", "York"}`

**Checking for Bad Arguments**  
We can use if statements in BASH to filter out bad arguments.  
To do this, we use an if statement with a *-z* flag to make sure an argument exists.  
```
if [ -z "$state" ]
then
    echo "Usage: $0 state"
    rm $temp_file
    exit 1
fi
```

**Parsing a File**  
We want to be able to grab what we want specifically from our data, without  
including unnecessary columns or lines.
- *head* allows us to grab the top of the file.
- *tail* allows us to grab the end of the file.  

Using these flags, piping, and a delimiter, we can not only cut out   
unnecessary pieces of the header like the state name and the 'fips' column,  
but we can also create an if-statement to validate that the state is in our data.  
```
# check to make sure the state exists within our file 
# first cut out unecessary parts of the file and then search for our state
state_check=$(tail +2 $temp_file | cut -d ',' -f 2 $temp_file | grep "$state")
if [ -z "$state_check" ] # if no such state exists
then   
    echo "No data for $state"
    rm $temp_file
    exit 2
fi

# output the header and cut out new york & 'fip' because it isnt necessary
head -n 1 $temp_file | cut -d , -f 1,4-5 
```
