# Write-a-Python-program-to-assess-if-a-file-is-closed-or-not.
def is_file_closed(file_path):
    try:
        file = open(file_path, 'r')
        file.close()
        return file.closed
    except FileNotFoundError:
        print("File not found.")
    except IOError:
        print("An error occurred while accessing the file.")

# Example usage
file_path = 'path/to/your/file.txt'  # Replace with the actual file path
closed = is_file_closed(file_path)
if closed is not None:
    if closed:
        print("The file is closed.")
    else:
        print("The file is open.")
