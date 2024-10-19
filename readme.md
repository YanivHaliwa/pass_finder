# Passwords_Finder: Advanced File Content Search Tool

PassF is a powerful and flexible Python-based utility designed for searching sensitive information within files. While it's particularly useful for cybersecurity professionals and system administrators who need to identify potential security risks in file contents, it's also an excellent tool for cybersecurity students and CTF (Capture The Flag) participants.

This versatile tool combines powerful search capabilities with customizable options, making it suitable for both professional security work and educational/competitive scenarios in cybersecurity.


**for more scripts related cyber and securiy check here: [Cyber Security Scripts section](https://github.com/YanivHaliwa/Linux-Stuff/blob/master/readme.md#cyber-security-scripts).**


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

 