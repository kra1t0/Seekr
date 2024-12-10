# Seekr

Seekr is a Python-based utility for recursively searching for keywords or sentences within all UTF-8 encoded files in a directory and its subdirectories. It supports case-insensitive searching, generates detailed reports, and performs cleanup of temporary directories after execution.

## Features

- Case-insensitive keyword search in UTF-8 encoded files.
- Generates a detailed report with matching file paths, line numbers, and content.
- Automatically excludes non-UTF-8 files to ensure compatibility.
- Cleanup of temporary directories after saving the report.
- Easy-to-use command-line interface.

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/kra1t0/Seekr.git
   cd Seekr
2. Install the Requirenments:
   ```bash
   pip install -r requirements.txt

To run use the python interpreter or just run casually as a script
```bash
./Seekr <keyword>
python3 Seekr <keyword>
```

## Example Usage

3.1 Search for the keyword password:
```
python3 Seekr password
```
Output:
```
Reading file: /path/to/file.txt
Match found in /path/to/file.txt on line 12: Password should be strong.
Reading file: /path/to/another_file.txt
Match found in /path/to/another_file.txt on line 5: Change your password regularly.
```


3.2 Search for a phrase:

```
python3 Seekr "error code"
```
Output:

```
Reading file: /logs/system.log
Match found in /logs/system.log on line 45: System encountered an error code 404.
```

The script will generate a report in the current directory with the following format:
```
report-error code.txt
```


4. Output and Cleanup
After the search is complete, the report is automatically saved in the parent directory of the script. The temporary directory used for report generation (keysearch-reports/) is deleted to keep your workspace clean

5. Requirements
Python 3.7+
Required Python modules are listed in requirements.txt.

6. Contributing
Contributions are welcome! If you'd like to add features or fix bugs, feel free to fork the repository and open a pull request.

