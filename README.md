# Terminal based File Explorer for Linux

### About
A fully functional File Explorer Application, albeit with a restricted feature set.
### Modes:
- Normal Mode
- Command Mode

	#### Normal Mode:
	Normal mode is the default mode of our application. It has the following functionalities -
	1. Display a list of directories and files in the current folder
		- Every file in the directory should be displayed on a new line with 						 
		the following attributes for each file - 
			- File Name 
			- File Size 
			- Ownership (user and group) and Permissions 
			- Last modified 
		All of this should be displayed in human readable format
	
		- The file explorer should show entries “.” and “..” for current and 	parent directory respectively
		- The file explorer should handle scrolling in the case of vertical overflow using keys k & l
		- User should be able to navigate up and down in the file list using the corresponding up and down arrow keys
	2. Open directories and files	
		
		When Enter key is pressed:
		- Directory - Clear the screen and navigate into the directory and show the directory contents as specified in point 1
		- File - Open the file in vi editor
	3. Traversal

		- Go back - Left arrow key should take the user to the previously visited directory
		- Go forward - Right arrow key should take the user to the next directory
		- Up one level - Backspace key should take the user up one level
		- Home - h key should take the user to the home folder (the folder where the application was started)	
	
	#### Command Mode
	The application should enter the Command button whenever “:” (colon) key is pressed. In the command mode, the user should be able to enter different commands. All commands appear in the status bar at the bottom.
		**1.** **Copy** - `copy <source_file(s)> <destination_directory>` 
			**Move** -  `move <source_file(s)> <destination_directory>`
			**Rename** - `rename <old_filename> <new_filename>`

	- E.g
    - `copy foo.txt bar.txt baz.mp4 ~/foobar` 
    - `move foo.txt bar.txt baz.mp4 ~/foobar` 
    - `rename foo.txt bar.txt`
    
   **2 .**  **Create File** - `create_file <file_name> <destination_path>`
			**Create Directory** - create_dir <dir_name> <destination_path>

	- `create_file foo.txt ~/foobar`
	- `create_file foo.txt .`
	- `create_dir foo ~/foobar` 



   **3.**  **Delete File** - `delete_file <file_path>`
			   **Delete Directory** - `delete_dir <dir_path>`
	
   **4.**  **Goto** - `goto <location>`

   **5.**  **Search** - `search <filename>` or `search <directory_name>` 
   	- Search for a given file or folder under the current directory recursively
   	- Output should be True or False depending on whether the file or folder exists
   
   **6.**  On pressing **ESC** key, the application should go back to Normal Mode
