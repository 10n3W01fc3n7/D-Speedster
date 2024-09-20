Project: Path Traversal Vulnerability Tester
Overview:
This project is a Python script designed to test web applications for potential path traversal vulnerabilities. It attempts to access restricted directories and files on a target system by manipulating URL paths.

Features:
Brute force directory traversal: The script attempts various directory traversal attacks by trying to access sensitive files such as system configuration files (/etc/passwd, /etc/shadow, etc.).
Customizable cookies: Allows the user to include optional cookies (like session IDs) when testing.
Automatic detection: If the file is accessible, it prints the success message along with the vulnerable URL.
File Structure:
expl.py: The main Python script containing the code for testing path traversal vulnerabilities.
Usage:
Pre-requisites:

Python 3.x
curl installed on the system
Running the script:

Run the script with:
bash
Copy code
python expl.py
The script will prompt you to:
Enter the URL of the target web application.
Optionally, provide cookies in the format PHPSESSID=value; security=value.
Process:

The script will attempt a series of path traversal attacks by appending different file paths to the provided URL.
For each attempt, the script will display whether the file was found or access was denied.
Example:
bash
Copy code
Enter the URL of the target website: http://example.com
Enter cookies (optional, PHPSESSID=value; security=value): PHPSESSID=12345; security=low
Brute forcing directory traversal...
Found: http://example.com/../../../../../../etc/passwd
Important Notes:
For ethical use only: Ensure you have permission before testing a website. Unauthorized testing may lead to legal consequences.
Customization: You can extend the list of directories being checked by adding more paths in the directories list in the script.
Contributing:
Feel free to open issues or submit pull requests if you have suggestions or improvements.

License:
This project is licensed under the MIT License.
