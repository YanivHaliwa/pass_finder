# Passwords_Finder: Advanced File Content Search Tool

PassF is a powerful and flexible Python-based utility designed for searching sensitive information within files. While it's particularly useful for cybersecurity professionals and system administrators who need to identify potential security risks in file contents, it's also an excellent tool for cybersecurity students and CTF (Capture The Flag) participants.

This versatile tool combines powerful search capabilities with customizable options, making it suitable for both professional security work and educational/competitive scenarios in cybersecurity.

## Key Use Cases

1. **Professional Security Audits**: Identify potential security risks in large codebases.
2. **CTF Challenges**: Quickly search for hidden flags or clues in CTF scenarios.
3. **Educational Tool**: Help cybersecurity students learn about information hiding and discovery techniques.
4. **System Administration**: Locate sensitive information across system files.


## Features

- **Keyword Search**: Search for specific keywords or patterns within files.
- **Configurable Search Depth**: Adjust the context around found keywords.
- **Comment Searching**: Option to specifically search within code comments.
- **Directory and File Exclusion**: Ability to exclude specific directories or files from the search.
- **Binary File Handling**: Automatically skips binary files to focus on text content.
- **Colored Output**: Uses color-coded console output for better readability.
- **JSON Configuration**: Supports loading search parameters from a JSON file.


### Installation

you can clone ONLY this folder if you run this command: 

```bash
git clone --filter=blob:none --no-checkout https://github.com/YanivHaliwa/Cyber-Stuff.git && cd Cyber-Stuff && git sparse-checkout init --cone && git sparse-checkout set pass_finder  && git checkout
```

OR you can Clone the repository using the following command:

```bash
git clone https://github.com/YanivHaliwa/Cyber-Stuff.git
cd Cyber-Stuff/pass_finder
```

## Usage
```
passf <target_folder> [options]
```

### Options

- `-g`, `--grep-length`: Set the context length around found keywords (default: 5).
- `-c`, `--comments`: Enable searching within comments.
- `-t`, `--tags`: Specify custom keywords (comma-separated).
- `-e`, `--exclude`: Specify directories or files to exclude (comma-separated).
- `-j`, `--json-file`: Use a JSON file for search configuration.

### Example JSON Configuration (ex.json)

```json
{
  "include": ["password", "api_key", "secret"],
  "exclude_dirs": [".git", "node_modules"],
  "exclude_files": ["*.log", "*.tmp"]
}
```

## Additional Utility: susfiles

The `susfiles` script is included in this folder to help you quickly identify files on your machine that may be considered suspicious or potentially sensitive. This tool is useful for:

- Locating files with names or extensions commonly associated with credentials, secrets, or other sensitive data
- Quickly auditing a system for files that may require further investigation

**Usage:**

```bash
./susfiles <target_folder>
```

This script is designed to complement the main password/content search tool by providing a fast way to surface files that warrant closer inspection.

## Author

Created by [Yaniv Haliwa](https://github.com/YanivHaliwa) for security testing and educational purposes.

