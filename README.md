
# CS6.302	Software Systems Development 
## Assignment 1 – Shell Programming & SQL

### Basic Setup and Usage

Before running the solutions, ensure your environment is properly configured.

#### Environment Requirements
- **Operating System**: Any modern OS (Linux, macOS, Windows), preferably Linux or any Unix-based system (recommended)
- **Shell**: Bash or a compatible shell to execute the provided scripts

#### Basic Configuration
1. **Ensure you have a shell environment** (e.g., Bash) installed and configured.
   - On Windows, you may use Git Bash or WSL (Windows Subsystem for Linux).

2. **Verify that shell scripts have executable permission** in your environment. If needed, grant execute permissions using:
   ```bash
   chmod +x script_name.sh
### Running the Solutions

Each question has its own folder, containing a shell script  that need to be run. The general steps are:

1. **Navigate to the desired question's folder** (e.g. `Q1/`, `Q2/`, `Q3/`, or `Q4/`):
   ```bash
   cd Q1
2. ***Run the provided shell script*** :
   ```bash
   ./Q1.sh

## Solution Description
### Q.1 Processing a given "Quotes" file
 ####  Input format

 You can run the script with the following syntax . Replace <file_name>  with the name of your input file. 
    ```bash
    ./Q1.sh <file_name>
Note: if no <file_name> is passed , default "quotes.txt" would be taken as file_name. If <file_name> invalid then file not found is shown. 


#### Output Generation

The script generates the following outputs:

- **Remove Empty Lines**:
  - Uses `grep -v '^$'` to filter out empty lines from the input file.
  - Outputs to `Q1_result/quotes_no_empty.txt`.

- **Remove Duplicates**:
  - Utilizes `awk` to remove duplicate lines and `sort -u` to ensure unique entries.
  - Outputs to `Q1_result/quotes_no_dups.txt`.

- **Count Quotes by Personality**:
  - Extracts the personality name from each line (assuming it's separated by `~`).
  - Counts the number of quotes per personality and appends this information to `Q1_result/quotes_by_personality.txt`.

- **List Words Starting with 's' but not followed by 'a'**:
  - Uses `grep` with a regex pattern to find words that start with 's' and are not followed by 'a'.
  - Outputs to `t.txt`.

### Q.2 Account Number and Password generator
 ####  Output Generation
The following script generates a random password and account number with fixed lengths and specific constraints.
 
##### Password Generation
- **Length**: Between 8 and 10 characters.
- **Constraints**:
  - At least one uppercase letter.
  - At least one lowercase letter.
  - At least one symbol.
- **Filling**: Remaining characters are random from a set of uppercase letters, lowercase letters, and symbols.

##### Account Number Generation
- **Length**: Between 12 and 14 digits.
- **Valid Digits**: `0, 4, 6, 7, 9`.
- **Constraints**:
  - No leading zeros.
  - Each digit appears a maximum of 3 times.

**Note**:  By choosing the digits from valid_digit set , no combination of 3 digit will form a Fibonacci series.

#### Q.3 Show Directory 
 ####  Output Generation

The script lists all directories in the current directory (where it is executed) and displays their sizes in ascending order.
##### Key Features 

 **Check for Directories:**
   - The script checks if there are any directories in the current directory using `ls -d */`. If no directories are found, it prints a message ("No directories found") and exits.

##### Q.4 Createa and handle Directory 
####  Output Generation

The script creates the required directory and performs manipulations using the "rename" command.

