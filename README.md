# WEEK-4-PYTHON
ASSIGNMENT
def read_and_write_file():
    input_filename = "input.txt"
    output_filename = "output.txt"
    
    try:
        # Read content from the input file
        with open(input_filename, "r") as infile:
            content = infile.read()

        # Modify the content (example: convert to uppercase)
        modified_content = content.upper()  # You can change this modification

        # Write the modified content to the output file
        with open(output_filename, "w") as outfile:
            outfile.write(modified_content)

        print(f"File '{input_filename}' has been read and modified content written to '{output_filename}'.")

    except FileNotFoundError:
        print(f"Error: The file '{input_filename}' was not found.")
    except IOError as e:
        print(f"Error reading or writing to file: {e}")

# Call the function
read_and_write_file()
def read_user_file():
    filename = "user_file.txt"  # Set the file name here

    try:
        # Try to open the file for reading
        with open(filename, "r") as file:
            content = file.read()
            print("File content:")
            print(content)

    except FileNotFoundError:
        print(f"Error: The file '{filename}' does not exist.")
    except IOError as e:
        print(f"Error: Could not read the file '{filename}'. Reason: {e}")

# Call the function
read_user_file()



