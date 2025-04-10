
# week-4-file-handling.py

#1. File Read & Write Challenge .Create a program that reads a file and writes a modified version to a new file.

myfile = "Tonny.txt"  # Original file to read
myfile2 = "Onwonga.txt"  # New file to write modified content

try:
    # Read the content from the original file
    with open(myfile, "r") as file:
        x= file.read()
        print(x)  # you can also use print(file.read()) directly  instead of assigning the read to x variable.

    # Modify the content (e.g., convert text to uppercase)
    y=x.upper() 

    # Write the modified content to the new file
    with open(myfile2, "w") as file:
        file.write(y)
  

   print("This are read and modified files")

except FileNotFoundError:
    print('File not found')
except Exception as e:
    print(f"Error occured")  #using f string formatting




#Question 2. Error Handling Lab .Ask the user for a filename and handle errors if it doesn’t exist or can’t be read.


x = input("Kindly enter file to read: ")  # The file to be read below.Notice the file inputted will be assigned to variable x

try:
    # Try to open and read the file
    with open(x, "r") as file:  # Open the file provided by user input
        material = file.read()  # Read the content of the file
        print("This is the content of the file:")
        print(material)

except FileNotFoundError:
    print(f"File '{x}' not found.")    #Additional f string formatting
except PermissionError:
    print('This file could not be opened due to permission issues.')
except Exception as e:
    print(f"An error occurred: {e}")    #Additional f string formatting




    
