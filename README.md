# Auto File Sorting and Undoing

## Project Overview
This project provides a Python script for automatically sorting files in a directory based on their types (file extensions). The script moves files into folders named after their respective file types (e.g., `.txt`, `.jpg`, etc.). Additionally, it includes functionality to undo the sorting by moving the files back to their original location.

### Features:
- **Sort Files**: Automatically categorizes files into folders based on their extensions.
- **Undo Sorting**: Allows you to move the files back to their original location, restoring the directory to its initial state.
- **Handles Common Errors**: Includes error handling for cases like missing files, permission issues, and unexpected errors during the file-moving process.

---

## Functionality

### 1. **sort_files(path)**
   - **Description**: Sorts files in the specified directory into subdirectories based on file types (extensions). It excludes system-related files (e.g., `.ini`).
   - **Steps**:
     - Identifies unique file types (extensions).
     - Creates folders for each unique file type.
     - Moves files into their respective folders.
   
### 2. **undo_sort(path)**
   - **Description**: Moves the files from the subdirectories back to the original directory, effectively undoing the sorting operation. It also removes any empty subdirectories.
   - **Steps**:
     - Identifies and moves files from subdirectories to the main directory.
     - Deletes any empty folders after moving the files back.

### 3. **user_choice()**
   - **Description**: Prompts the user to either sort files or undo sorting based on their input.
   - **Steps**:
     - Asks the user to input a choice (1 for sorting, 2 for undoing).
     - Based on the choice, calls either the `sort_files()` or `undo_sort()` function.

---

## How to Use

1. **Run the Program**:
   - The program prompts the user to choose between sorting files or undoing the sorting operation.

2. **Sort Files**:
   - If you choose to sort the files, enter the path to the directory containing the files. The script will sort all files into folders based on their extensions (e.g., `.txt`, `.jpg`).

3. **Undo Sorting**:
   - If you want to undo the sorting, enter the path to the directory where the files were sorted. The script will move all files back to the original location and remove the created subdirectories.

---

## Error Handling:
- **FileNotFoundError**: Raised if no files are found in the specified directory.
- **PermissionError**: Raised if the script doesn’t have the necessary permissions to move files or access directories.
- **General Exception Handling**: Catches any unexpected errors that occur during the process.

---

## Example

### Example 1: Sorting Files
```bash
Do you want to (1) Sort files or (2) Undo sorting? Enter 1 or 2: 1
Enter the path to the directory to sort files: /path/to/your/directory
