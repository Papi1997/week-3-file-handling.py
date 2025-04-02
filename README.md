# week-3-file-handling.py

#1. File Read & Write Challenge .Create a program that reads a file and writes a modified version to a new file.

myfile = "Tonny.txt"  # Original file to read
myfile2 = "Onwonga.txt"  # New file to write modified content

try:
    # Read the content from the original file
    with open(myfile, "r") as file:
        x= file.read()

    # Modify the content (e.g., convert text to uppercase)
    y=x.upper() 

    # Write the modified content to the new file
    with open(myfile2, "w") as file:
        file.write(y)

    print("This are read and modified files")

except FileNotFoundError:
    print('File not found')
except Exception as e:
    print(f"Error occured")


    
