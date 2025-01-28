# File Unzipper + Zipper

A lightweight PHP-based application that enables you to compress files into zip archives or extract files from `.zip`, `.rar`, and `.gz` archives. This program is ideal for handling basic file archiving tasks on your server.

## Features

- Extract files from `.zip`, `.rar`, and `.gz` archives.
- Compress directories into `.zip` files.
- Simple and intuitive web interface.
- Displays processing time and status messages.

## Prerequisites

- PHP 7.4 or higher.
- The following PHP extensions:
  - `ZipArchive` for `.zip` files.
  - `zlib` for `.gz` files.
  - `rar` for `.rar` files (if not installed, see the [PHP manual](http://php.net/manual/en/rar.installation.php)).

## Installation

1. Clone or download this repository to your web server's directory:
   ```bash
   git clone https://github.com/auslui/PHP-Unzipper.git
   ```

2. Ensure the web server has write permissions to the directory where the script is hosted.

3. Open the directory in your browser.

## Usage

### Extracting Archives

1. Select a `.zip`, `.rar`, or `.gz` file from the dropdown menu.
2. Optionally, specify an extraction path (relative to the current directory).
3. Click the **Unzip Archive** button.

### Creating Archives

1. Enter the path of the folder to compress (relative to the current directory). Leave empty to compress the current directory.
2. Click the **Zip Archive** button.

### Notes

- The extraction path must be writable by the web server.
- If a `.gz` archive contains a `.tar` file, the program will extract the `.tar` contents and remove the intermediate `.tar` file.

## Output

- Status messages are displayed at the top of the page, indicating success or errors.
- Processing time is also displayed.

## Security Considerations

- Ensure the script is not exposed to public access on a production server.
- Always validate the archives before uploading to prevent malicious content.

## Known Issues

- `.rar` extraction requires the `rar` PHP extension, which may not be enabled by default.
- Extraction and compression operations are limited by the server's file and memory limits.

## Author

[Austine Luis](https://github.com/auslui)
