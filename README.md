# Log Analyzer

A desktop application designed for analyzing Apache web server log files through a user-friendly graphical interface.
-----

## Features

  * **Parse Apache Common Log Format files**: Accurately extracts data from standard Apache logs.
  * **Generate detailed traffic analytics**: Provides insights into web traffic patterns.
  * **Track IP addresses, endpoints, and status codes**: Identifies key metrics for analysis.
  * **Export results in TXT or JSON format**: Allows for flexible data sharing and integration.
  * **Real-time progress tracking**: Displays processing status for large files.
  * **Comprehensive error handling**: Manages common issues like invalid file types or formats.

-----

## Requirements

  * **Python 3.6 or higher**
  * **tkinter**: Typically included with Python installations.
  * **Standard Python libraries**: `re`, `json`, `datetime`, `collections`, `threading`, `os`, `mimetypes`.

-----

## Installation

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/log-analyzer.git
    cd log-analyzer
    ```
2.  **Ensure Python is installed** on your system:
    ```bash
    python --version
    ```
3.  **No additional packages needed**: The application relies solely on built-in Python libraries.

-----

## How to Run

### Method 1: Command Line

```bash
python log_analyzer.py
```
### Method 2: IDE

  * Open the `main.py` file in any Python IDE (e.g., PyCharm, VS Code).
  * Execute the script directly from the IDE.

-----

## Usage Instructions

1.  **Launch the application**: The GUI window titled "Log Analyzer" will appear.
2.  **Select a log file**: Click the "Browse" button and choose a `.txt` file containing Apache Common Log Format entries. Only `.txt` files are supported.
3.  **Analyze the file**: Click the "Analyze" button. A progress bar will indicate the processing status, and results will be displayed in the text area below.
4.  **Export results (optional)**:
      * Click "Export as TXT" for a human-readable format.
      * Click "Export as JSON" for a machine-readable format.
      * Choose your desired save location and filename.
5.  **Clear results (optional)**: Click "Clear Results" to reset the display.

-----

## Supported Log Format

The application expects Apache Common Log Format, which follows this structure:

```
IP - - [timestamp] "METHOD /path HTTP/version" status_code response_size
```

**Example**:

```
192.168.1.1 - - [25/Dec/2023:10:30:45 +0000] "GET /index.html HTTP/1.1" 200 1234
```

-----

## Sample Output

The analysis provides the following key metrics:

  * **Summary**: Total requests, unique IP addresses, and error rates.
  * **Top IP Addresses**: A list of the most active visitors.
  * **Status Code Distribution**: A breakdown of success and error codes.
  * **Top Endpoints**: The most frequently requested web pages.
  * **Analysis Period**: The time range covered by the processed logs.

-----

## Troubleshooting

**"Invalid file type" error**:

  * Ensure your log file has a `.txt` extension.
  * Convert other log file formats to `.txt` if necessary.

**"File validation failed" error**:

  * Verify that the file contains valid Apache log entries.
  * Confirm that at least 10% of the lines match the expected log format.

**GUI doesn't appear**:

  * Check if tkinter is installed by running `python -c "import tkinter"` in your terminal.
  * Try executing the script using `python3` instead of `python`.

**Large files taking too long**:

  * The application processes files line by line, and the progress bar shows the current status.
  * Very large files (exceeding 100MB) may require several minutes to process, depending on system performance.

-----

## File Size Recommendations

  * **Small files** (\< 1MB): Typically processed instantly.
  * **Medium files** (1-50MB): Analysis usually takes a few seconds.
  * **Large files** (50MB+): Processing time may extend to several minutes, depending on system specifications.

-----

## Author

Created for an internship task at Omukk.

-----

## Acknowledgments

  * Built with Python's tkinter for cross-platform compatibility.
  * Designed specifically for Apache Common Log Format analysis.
  * Optimized for efficient performance, even with large log files.
