--------------------------------------------------------------------------------------------------------------------------
**Algorithm for file updates in Python**
--------------------------------------------------------------------------------------------------------------------------

--------------------------------------------------------------------------------------------------------------------------
Project description
--------------------------------------------------------------------------------------------------------------------------
An important part of cybersecurity is controlling access to restricted content. In this project, I have worked with a text file containing IP addresses that are allowed to access specific restricted content in a hypothetical organization.

Parsing a file allows security analysts to read and update the contents. Python helps analysts develop algorithms to automate the process of parsing files and keeping them up-to-date.

I have developed an algorithm that parses this text file of IP addresses and updates the file by removing that addresses that no longer have access to the restricted content.

--------------------------------------------------------------------------------------------------------------------------
Open the file that contains the allow list
--------------------------------------------------------------------------------------------------------------------------
The file that I want to open is called "allow_list.txt". I assigned a string containing this file name to the import_file variable. Then, used a with statement to open it. I used the variable to store the file while I work with it inside the with statement.


--------------------------------------------------------------------------------------------------------------------------
Convert the string into a list
--------------------------------------------------------------------------------------------------------------------------
In order to remove individual IP addresses from the allow list, the IP addresses need to be in a list format. Therefore, I used the .split() method to convert the ip_addresses string into a list.

--------------------------------------------------------------------------------------------------------------------------
Iterate through the remove list
--------------------------------------------------------------------------------------------------------------------------
A second list called remove_list contains all of the IP addresses that should be removed from the ip_addresses list. The header of a for loop that will iterate through the remove_list. Used element as the loop variable.

--------------------------------------------------------------------------------------------------------------------------
Remove IP addresses that are on the remove list
--------------------------------------------------------------------------------------------------------------------------
In the body of the iterative statement, I added code that will remove all the IP addresses from the allow list that are also on the remove list. First, I created a condition that evaluates if the loop variable element is part of the ip_addresses list. Then, within that conditional, I appled the .remove() method to the ip_addresses list and remove the IP addresses identified in the loop variable element. 

--------------------------------------------------------------------------------------------------------------------------
Update the file with the revised list of IP addresses
--------------------------------------------------------------------------------------------------------------------------
Now that I have removed these IP addresses from the ip_address variable, I can complete the algorithm by updating the file with this revised list. To do this, I must first convert the ip_addresses list back into a string using the .join() method. Apply .join() to the string "\n" in order to separate the elements in the file by placing them on a new line.

Then, used another 'with' statement and the .write() method to write over the file assigned to the import_file variable.

--------------------------------------------------------------------------------------------------------------------------
Summary
--------------------------------------------------------------------------------------------------------------------------

Python has functions and syntax that help to import and parse text files.
- The with statement allows to efficiently handle files.
- The open() function allows to import or open a file. It takes in the name of the file as the first parameter and a string that indicates the purpose of opening the file as the second parameter.
- Specify "r" as the second parameter if you're opening the file for reading purposes.
- Specify "w" as the second parameter if you're opening the file for writing purposes.
- The .read() method allows to read in a file.
- The .write() method allows to append or write to a file.
- You can use a for loop to iterate over a list.
- You can use an if statement to check if a given value is in a list and execute a specific action if so.
- You can use the .split() method to convert a string to a list.
- You can use Python to compare contents of a text file against elements of a list.
- Algorithms can be incorporated into functions. When defining a function, you must specify the parameters it takes in and the actions it should execute.

