# Address Book 
The "Address Book" project is a command-line interface (CLI) tool designed to manage a simple address book. This utility allows users to create, display, insert, modify, delete, and search records within a text file. Each record consists of a roll number and a name, offering basic functionality to maintain and manage a list of contacts efficiently. The tool uses standard Unix/Linux shell commands and utilities, making it lightweight and easy to use on any system with a shell environment.

# Motivation
The motivation behind creating the "Address Book" project stems from the need for a simple yet effective way to manage contact information without the overhead of complex database systems or graphical user interfaces. It is particularly useful for educational purposes, demonstrating fundamental file handling and text processing techniques in Unix/Linux. Additionally, it serves as a practical tool for users who prefer working in a CLI environment and require a straightforward method to keep track of contact information

# Design Goals/Objectives
The primary objectives of the "Address Book" project are:
Create an Address Book: Implement a function to create a new address book file, ensuring that no duplicate files are created.
Display Address Book: Provide functionality to display the contents of the address book in a readable format.
Insert Records: Enable users to add new records, ensuring no duplicate roll numbers are inserted.
Modify Records: Allow users to modify existing records by updating the name associated with a specific roll number.
Delete Records: Implement a method to delete specific records based on roll number, ensuring the correct record is removed.
Search Records: Provide a search function to find and display records based on roll number.
User-Friendly Interface: Create an intuitive and easy-to-use interface that guides users through various operations with clear instructions and feedback.

# Tools we use
The "Address Book" project leverages several essential Unix/Linux tools and commands to efficiently manage contact information through a shell script. The primary tool is Bash, which provides a scripting environment for automating tasks and managing files. The touch command is used to create new address book files, while echo outputs text for user prompts and feedback. To display the contents of the address book, the cat command is employed. The script uses grep to search for specific roll numbers and sed to modify or delete records within the file. Conditional logic is implemented using if statements to check for the existence of files and records, and a while loop creates an interactive main menu that prompts the user until they choose to exit. User choices are handled by a case statement, directing the flow to the appropriate function. Additionally, the read command is essential for capturing user input for file names, roll numbers, names, and menu selections. Together, these tools and commands create a cohesive and user-friendly command-line application for managing an address book.

# Conclusion
The "Address Book" project successfully demonstrates the use of Unix/Linux shell scripting to manage a simple contact management system through a command-line interface. By utilizing fundamental tools and commands, the project provides an efficient and user-friendly way to create, display, insert, modify, delete, and search records within a text file. Each function is carefully designed to handle specific tasks, ensuring data integrity and ease of use. The project achieves its goal of offering a practical, lightweight solution for managing contact information without the need for complex databases or graphical interfaces.
