# ASSIGNMENT-WEEK-4
TASK 1
def modify_file_content(input_filename, output_filename):
    try:
        # Open the input file in read mode
        with open(input_filename, 'r') as infile:
            # Read the content of the file
            content = infile.read()

        # Modify the content (for example, converting to uppercase)
        modified_content = content.upper()

        # Open the output file in write mode
        with open(output_filename, 'w') as outfile:
            # Write the modified content to the new file
            outfile.write(modified_content)

        print(f"Content has been modified and written to {output_filename}")
    
    except FileNotFoundError:
        print(f"Error: The file {input_filename} does not exist.")
    except Exception as e:
        print(f"An unexpected error occurred: {e}")


# Ask the user for filenames
input_filename = input("Enter the name of the file to read: ")
output_filename = input("Enter the name of the new file to save the modified content: ")

# Call the function to modify and write the file
modify_file_content(input_filename, output_filename)

#TASK 2
def read_file_with_error_handling():
    try:
        # Ask user for filename
        filename = input("Enter the filename to read: ")

        # Open the file in read mode
        with open(filename, 'r') as file:
            content = file.read()

        print("File content:")
        print(content)

    except FileNotFoundError:
        print(f"Error: The file {filename} does not exist.")
    except PermissionError:
        print(f"Error: You do not have permission to read the file {filename}.")
    except Exception as e:
        print(f"An unexpected error occurred: {e}")


# Call the function to read a file
read_file_with_error_handling()
