# plp_fille_week_5_ass
File Read &amp; Write Challenge 🖋️: Create a program that reads a file and writes a modified version to a new file. Error Handling Lab 🧪: Ask the user for a filename and handle errors if it doesn’t exist or can’t be read.
try:
    input_filename = "input.txt"
    output_filename = "output.txt"

    # Read the file content and count the words in one go
    with open(input_filename, 'r') as infile:
        content = infile.read()
        word_count = len(content.split())
        uppercase_content = content.upper()
    
    # Write the processed data to the output file
    with open(output_filename, 'w') as outfile:
        outfile.write(f"Word Count: {word_count}\n\n")
        outfile.write(uppercase_content)
    
    print(f"Success! The file '{output_filename}' has been created.")

    except FileNotFoundError:
        print(f"Error: The file '{input_filename}' was not found.")
    except Exception as e:
        print(f"An unexpected error occurred: {e}")
