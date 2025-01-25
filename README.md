LeetCode Fetcher Chrome Extension
The LeetCode Fetcher is a user-friendly Chrome extension designed to streamline working with LeetCode problems. It helps you effortlessly extract test cases, generate solution files, and test your solutions directly, making your problem-solving workflow more efficient.
________________________________________
Key Features
•	Auto-Detection of LeetCode Problem URLs: Automatically recognizes the open LeetCode problem page.
•	Language Selection: Choose between Python (.py) and C++ (.cpp) for your solution files.
•	Test Case Extraction: Extracts test cases from the problem page and saves them as a test_cases_named.json file.
•	Boilerplate Generation: Creates a starter solution file in the selected programming language.
•	Solution Testing: Easily test your solutions with predefined test cases using the included test.py script and VS Code integration.
________________________________________
Installation Guide
Step 1: Clone or Download the Repository
Clone this repository or download its contents to your local machine.
Step 2: Install the Chrome Extension
1.	Open Chrome and navigate to chrome://extensions/.
2.	Enable Developer mode in the top-right corner.
3.	Click Load unpacked, then select the folder containing the extension files.
Step 3: Set Up the API Server
1.	Ensure Python is installed on your system.
2.	Install the required Python packages by running:
bash
CopyEdit
pip install flask cloudscraper beautifulsoup4
3.	Start the Flask server by executing:
bash
CopyEdit
python app.py
4.	The server will run at http://127.0.0.1:5000.
________________________________________
How to Use
Running the Extension
1.	Open a LeetCode problem page in Chrome.
2.	Click the LeetCode Fetcher extension icon in the toolbar.
3.	Choose your desired programming language (Python or C++) when prompted.
4.	The extension will generate the test cases and a solution file in the default directory.
Folder Structure
The generated files are organized within a leetcode directory (or another folder name defined in fetch.py). The structure resembles:
bash
CopyEdit
/leetcode/
├── two-sum/
│   ├── test_cases_named.json
│   ├── solution.py
│   ├── solution.cpp
├── test.py
└── .vscode/
    └── tasks.json
________________________________________
Testing Your Solution
Prerequisites
1.	Place the provided test.py file inside the leetcode folder.
2.	Create a .vscode folder within the leetcode directory and add the supplied tasks.json file.
Running Tests in VS Code
1.	Open VS Code and navigate to the solution file (e.g., solution.py or solution.cpp).
2.	Press Ctrl+Shift+P (or Cmd+Shift+P on Mac) and select Tasks: Run Task.
3.	Choose Test Current Solution from the task list.
4.	The test results will appear in the terminal output.
________________________________________
Important Notes
1.	Folder Setup: Ensure the leetcode directory exists at the specified path. If you rename it, update the path in fetch.py.
2.	tasks.json Configuration: The tasks.json file configures VS Code to run the test.py script with the solution file.
3.	Language Selection: Make sure to choose the correct language (Python or C++) when using the extension to generate solution files.
