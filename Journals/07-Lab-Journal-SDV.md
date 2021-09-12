- # SDV601 - Week 7 Blog

  ------

  #### <u>Setting Up the Development Environment, Variables, and Code Convention</u>

  ------

  What have I learned?

  Although I have already done file manipulation, this week I improved my skills and understanding of file manipulation in Python. Like the name suggests, the concept of file manipulation revolves around anything to do with files whether it is opening and viewing the data, adding to the data, updating existing data, deleting data, saving to new files, or copying files (to name a few). 

  

  Tutorialspoint (n.d.)

  Here is a list of the different modes of opening a file −

  |      |                     Modes & Description                      |
  | :--: | :----------------------------------------------------------: |
  |  1   | **r**<br />Opens a file for reading only. The file pointer is placed at the beginning of the file. This is the default mode. |
  |  2   | **rb**<br />Opens a file for reading only in binary format. The file pointer is placed at the beginning of the file. This is the default mode. |
  |  3   | **r+**<br />Opens a file for both reading and writing. The file pointer placed at the beginning of the file. |
  |  4   | **rb+**<br />Opens a file for both reading and writing in binary format. The file pointer placed at the beginning of the file. |
  |  5   | **w<br />**Opens a file for writing only. Overwrites the file if the file exists. If the file does not exist, creates a new file for writing. |
  |  6   | **wb**<br />Opens a file for writing only in binary format. Overwrites the file if the file exists. If the file does not exist, creates a new file for writing. |
  |  7   | **w+**<br />Opens a file for both writing and reading. Overwrites the existing file if the file exists. If the file does not exist, creates a new file for reading and writing. |
  |  8   | **wb+<br />**Opens a file for both writing and reading in binary format. Overwrites the existing file if the file exists. If the file does not exist, creates a new file for reading and writing. |
  |  9   | **a<br />**Opens a file for appending. The file pointer is at the end of the file if the file exists. That is, the file is in the append mode. If the file does not exist, it creates a new file for writing. |
  |  10  | **ab**<br />Opens a file for appending in binary format. The file pointer is at the end of the file if the file exists. That is, the file is in the append mode. If the file does not exist, it creates a new file for writing. |
  |  11  | **a+<br />**Opens a file for both appending and reading. The file pointer is at the end of the file if the file exists. The file opens in the append mode. If the file does not exist, it creates a new file for reading and writing. |
  |  12  | **ab+<br />**Opens a file for both appending and reading in binary format. The file pointer is at the end of the file if the file exists. The file opens in the append mode. If the file does not exist, it creates a new file for reading and writing. |

  **Examples**

  1. Appending

     ```python
     f = open("test.txt", "a") #Opens the file if exists, else creates a new file
     f.write("This is appeneded to the end of the file")
     f.close()
     
     f = open("test.txt", "r") #Opens the file as read only
     print(f.read()) #Prints the contents of the file
     ```

  2. Overwriting

     ```python
     f = open("test2.txt", "w") #Opens the file if exists, else creates a new file
     f.write("This has overwritten the files content")
     f.close()
     
     f = open("test2.txt", "r") #Opens the file as read only
     print(f.read()) #Prints the contents of the file
     ```

  3. Updating rows

     ```python
     import csv
     
     with open('./test3') as inf:
         reader = csv.reader(inf.readlines())
     
     with open('./test3', 'w') as outf:
         writer = csv.writer(outf)
         for line in reader:
             if line[1] == '0':
                 writer.writerow(line[0], '1')
                 break
             else:
                 writer.writerow(line)
         writer.writerows(reader)
     ```

  4. Deleting File

     ```python
     import os
     if os.path.exists("test4.txt"):
       os.remove("test4.txt")
     ```

  5. Copying File

     ```python
     from shutil import copyfile
     copyfile(source, destination)
     #The destination location must be writable; otherwise, an IOError exception will be raised.
     #If destination already exists, it will be replaced.
     ```

  

  How have I learned this?

  These are basic skills we should know as these are common tasks that applications will perform. There are many scenarios where it will be useful to implement these techniques.


  ------

  Why have I learned this?

  I have learned this by watching YouTube videos and reading the python documentation to understand how to implement the code. i also looked at examples of where and how we can use file manipulation.


  ------

  What will I do to remember this learning?
  I will continue to practice these skills and find ways to implement file manipulation into my projects.

  ------

  What do I know now, that I did not know before?

  I had already done a fair bit of file manipulation prior to these lessons, thus there isn't anything that comes to mind that I have learned.



Tutorialspoint. (n.d.). *Python - Files I/O*. Retrieved September 12, 2021, from https://www.tutorialspoint.com/python/python_files_io.htm
