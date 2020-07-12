# Bruteforce_using_Python
Brute force attack using Python:
Step 1:
Create a text file : file.txt

Step 2:
Create a password protected zip file:
Command: zip --password (type_password_here) (zipfilename).zip file.txt
 

Step 3:
Move file.txt to some other folder or delete file.txt

Step 4:
Python code:

import zipfile

filename= 'zipfile.zip'
dictionary = 'pass_list.txt'
password = None
file_to_open= zipfile.ZipFile(filename)
with open(dictionary, 'r') as f:
    for line in f.readlines():
        password = line.strip('\n')
        try:
            file_to_open.extractall(pwd=password)
            password = 'Password found: %s ' % password
            print (password)
        except:
            pass



Step 5:
Run code

Step 6:
Cat file.txt

OUTPUT:
goodjob!
