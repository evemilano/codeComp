# Theme Comparison Script

This script is designed to extract, compare, and report differences between two themes contained in zip files. It compares the files within the themes and generates a detailed report of any missing, added, or modified files.

## Features

- Extracts zip files in a specified input directory.
- Compares the files between two themes.
- Generates a detailed report of missing, added, and modified files.
- Outputs the report to a text file with a timestamp.

## Requirements

- Python 3.x

## Installation

1. Clone the repository:
   git clone https://github.com/yourusername/theme-comparison-script.git
   cd theme-comparison-script

2. Install the dependencies:
   pip install pygame paramiko

3. Setup your configuration:
   Modify the variables log_file, ip, user, and keys_folder in the script to match your server's details.

## Configuration

- input_folder: This is the directory where your theme zip files should be placed. The default is set to "input".

## Code Explanation

- extract_zip_files(input_folder): This function extracts all zip files found in the specified input directory.

- get_all_files(folder): This function retrieves a set of all file paths within the specified folder, relative to the folder's root.

- compare_files(file1, file2): This function compares two files and returns the differences in a unified diff format.

- generate_report(theme1, theme2): This function compares the files between two themes and generates a report detailing missing, added, and modified files.

- main(): The main function that orchestrates the extraction, comparison, and report generation process.

## Report Format

The generated report includes:
- Missing files in the second theme compared to the first.
- Added files in the second theme compared to the first.
- Modified files with detailed line-by-line differences.
