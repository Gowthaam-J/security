# Static Evaluation Report

## Prompt 1:
**Input:**
```
Create a new Git branch and switch to it.
```

**Base Model Output:**
```
1. Open a terminal window.
2. Run the following command to create a new Git commit:
   ```
   git commit -m "Adding feature"
   ```

   This command will create a new commit with a message that explains the purpose of the change.

   The command will add a new commit to the current branch with the name
```

**Fine-Tuned Model Output:**
```
1. Switch to a new branch. This can be done using `git checkout -b my_new_branch_name`.
2. Make changes on the branch.
3. Commit and push the changes to the remote repository.
4. Switch back to the main branch using `git checkout main`.

I hope these tips and tricks help you get started with GitHub!
```

**BLEU Score:** `0.0`

**ROUGE-L Score:** `0.2569`

**Dry-Run Commands:**
```bash
echo git checkout -b my_new_branch_name
echo git checkout main
```

---

## Prompt 2:
**Input:**
```
Compress the folder reports into reports.tar.gz
```

**Base Model Output:**
```
1. Create a new folder named reports in the root folder of the project and add all the report files into the reports folder.
2. Tar the folder reports into reports.tar.gz.
3. Use tar command with the -f flag to compress the reports.tar.gz file to a new folder named reports-compressed in the root folder of the project.
4. Open the reports-compressed folder in your text editor to view the contents of the report files.

5. To extract the reports from the reports-compressed folder, run the following command:

    ```
    tar -xvf reports-compressed/reports.tar.gz -C reports/
    ```

    Replace reports.tar.gz with the name of the compressed folder from the previous step.

That's it! You have successfully compressed your report files into a compressed folder with ease.
```

**Fine-Tuned Model Output:**
```
1. Open Terminal (Mac)
2. Run `tar -czvf reports.tar.gz reports` command in terminal to compress folder reports into reports.tar.gz
3. After the process is complete, you will have a compressed report in reports.tar.gz
4. Access the compressed report file using any web browser

5. Check if report has been compressed successfully by running `tar -zcat reports.tar.gz` command in terminal
If report is successfully compressed, the terminal will display report.tar.gz file size, and the file will be in.gz format with.tar.gz extension.

6. If report file size is not as expected, you can resize the tarball by adding `-z` flag to the `tar` command.
```
$ tar -czvf reports.tar.gz reports
```

7. Verify the report file is located at the expected directory by running `ls -lh` command in terminal.

With these steps, you can zip report archive in terminal.
```

**BLEU Score:** `0.0412`

**ROUGE-L Score:** `0.2827`

**Dry-Run Commands:**
```bash
echo tar -czvf reports.tar.gz reports
echo tar -zcat reports.tar.gz
echo tar
echo ls -lh
```

---

## Prompt 3:
**Input:**
```
List all Python files in the current directory recursively.
```

**Base Model Output:**
```
1. Create a file named `find_and_copy.bat` in the same directory as the Python file.
2. Paste the following code into the batch file:
```
python find_python_files.py
shutdown /s /r /f
```
3. Save the file as `find_and_copy.bat`.
4. Set the `START` environment variable to point to the location of the batch file.
```
SET START=C:\Python36\Scripts
```
5. Run the batch file to run the find and copy action.
```
start %START% find_and_copy.bat
```

Note: This example only demonstrates the core functionality of the modules; detailed explanations can be found in the respective documentation.
```

**Fine-Tuned Model Output:**
```
1. Create a new empty Python file.
2. In the new file, import the os module.
3. Use the os module to get the file names of all Python files in the current directory.
4. Sort the file names using the sorted() function and print the sorted file names.

Here's the code:

```python
import os

# Get the file names of all Python files in the current directory
file_names = [os.path.join(os.getcwd(), f) for f in os.listdir(os.getcwd()) if os.path.isfile(f)]

# Sort the file names using the sorted() function
file_names.sort()

# Print the sorted file names
print(file_names)
```

That's it! This program will create a new empty Python file in the current directory and prompt the user to enter the path to the directory containing the files. It will then use the `os.listdir` and `os.path.isfile` functions to get all file names and sort them using the `sorted` function. Finally, it will print the sorted file names to the console.
```

**BLEU Score:** `0.0666`

**ROUGE-L Score:** `0.2409`

---

## Prompt 4:
**Input:**
```
Set up a virtual environment and install requests.
```

**Base Model Output:**
```
1. Import the requests module as shown below:

```python
import requests
```

2. Make an HTTP request by sending a GET request to the API endpoint.

```python
response = requests.get('https://example.com/api/data')
```

3. Get the JSON data from the response.

```python
data = response.json()
```

4. Print the data.

```python
print(data)
```

That's it! You now have a Python program that makes HTTP requests to an API endpoint using the requests library.
```

**Fine-Tuned Model Output:**
```
1. Open your terminal
2. Write "python3 -m pip install requests"
3. Wait for the installation to complete.

Step 2: Set up the Google Sheets API
Once the virtual environment is setup, you can set up the Google Sheets API. Open the Google Sheets script editor and create a new sheet with a sample data.

Step 3: Import requests and make an API request
Next, you will need to import the requests module. Open the Google Sheets script editor again and create a new cell.

In this cell, write:

```python
import requests
```

Step 4: Set up a URL and make an API request
You can now make an API request to the Google Sheets API.

First, replace the placeholder `YOUR_ACCOUNT_ID` with your own account ID.

```python
url = f"https://sheets.googleapis.com/v4/{YOUR_ACCOUNT_ID}/spreadsheets/my_sheet_id"
data = {'values': {'!$B$2:B$10': ['data']}}
headers = {'Authorization': 'Bearer YOUR_API_KEY'}
response = requests.post(url=url, data=data, headers=headers)
print(response.status_code)
```

Replace `YOUR_API_KEY` with your own API key.

Step 5: Output the response data
Finally, output the response data to the Google Sheets spreadsheet.

```python
response.json()
```

Step 6: Clean up the script and exit the script
Finally, make sure to clean up any temporary files or scripts you may have created.

```python
exit()
```

These are the steps to create a Python program to automate a Google Sheets script using the Google Sheets API. Follow the above instructions to set up the virtual environment and install requests, then import the requests module, set up a URL and make an API request, set up a virtual environment, and make an API request.

Hopefully, these steps will help you get started with automating your Google Sheets script using the Google Sheets API!
```

**BLEU Score:** `0.0766`

**ROUGE-L Score:** `0.2091`

---

## Prompt 5:
**Input:**
```
Fetch only the first ten lines of a file named output.log.
```

**Base Model Output:**
```
1. First, we read the contents of output.log into a string variable using the `readln` function.

2. Then, we remove any leading or trailing spaces from the string using the `trim` function.

3. Finally, we split the string by `;` into an array of words, by separating each word with a comma.

4. If the number of words in the array is less than ten, we output a message indicating that there are fewer than ten words.

5. If the number of words in the array is greater than or equal to ten, we output the first ten words in the array.

6. Finally, we call the `println` function to display the output.
```

**Fine-Tuned Model Output:**
```
1. Open the terminal and navigate to the directory where the file to be processed exists.
2. Create a new text file named output.log.
3. In the Terminal, type the following command and press Enter:

```
tail -n 10 output.log
```

4. The output will appear in your new text file named output.log.
5. You can save this file by clicking on the “Save” button on your preferred text editor.

Note: The “-n 10” flag in the tail command means to only display the first 10 lines of the file.
```

**BLEU Score:** `0.0`

**ROUGE-L Score:** `0.1765`

---

## Prompt 6:
**Input:**
```
Find and delete all .pyc files within the current directory and its subdirectories.
```

**Base Model Output:**
```
1. Create an empty script:
```python
from os.path import isfile, join, rmdir

def delete_all_pyc():
    for f in [f for f in rmdir(join(join(join(r'..', '..', '..'), '__pycache__'), '*'), recursive=True)] if isfile(f):
        os.remove(f)

delete_all_pyc()
```
2. Add this script to your python file:
```python
import os
import sys

def delete_all_pyc():
    for f in [f for f in rmdir(join(join(join(r'..', '..', '..'), '__pycache__'), '*'), recursive=True)] if isfile(f):
        os.remove(f)

if __name__ == '__main__':
    try:
        delete_all_pyc()
    except Exception as e:
        print('Unable to delete.pyc files:', e)
        exit()

sys.exit(0)
```

3. Add the script to your `.pyc` file (in this case it is in your project folder), for example `./myscript.pyc`

4. Test:
```bash
$ python3 myscript.py
```

5. To make the deletion permanent, you can add the following line to your `~/.bashrc` file:
```bash
export PYTHONPATH="$PYTHONPATH:$HOME/dev/my_project/src"
```

I hope this helps!
```

**Fine-Tuned Model Output:**
```
1. Open your terminal or command prompt.
2. Change into the directory where you want to find and delete.pyc files.
3. Run the following command:

```bash
find. -name '*.pyc' -exec rm {} +
```

Replace `*.pyc` with the file extension (e.g., `*.py`, `*.pyc`, etc.).

This command searches for all.pyc files in the current directory and its subdirectories. It then removes each file by renaming it to its original filename (i.e., without the extension).

When you want to remove all.pyc files in the current directory, add a **+** in front of the command:

```bash
find. -name '*.pyc' -exec rm {} +
```

Remember to replace `*.pyc` with the file extension.

Tips:
- Use `find` in combination with `and` or `or` filters to filter out files based on a condition.
- To find and delete.pyc files globally (i.e., not just within the current directory), use a combination of `-name` and `-type d` or `-type f`.

Hope this helps!
```

**BLEU Score:** `0.0405`

**ROUGE-L Score:** `0.1672`

---

## Prompt 7:
**Input:**
```
Extract the contents of archive.tar.gz to a folder named extracted, creating the folder if it doesn’t exist.
```

**Base Model Output:**
```
1. Install PHP

a) Download and extract the PHP zip archive from https://www.php.net/downloads.php (you can use a file browser or the web interface)

b) Extract the contents of the downloaded file to a folder on your computer named “php”.

c) Create a new PHP script file and save it with a.php extension.

2. Install Git and Composer

a) Download and extract the Git zip archive from https://git-scm.com/downloads (you can use a file browser or the web interface)

b) Extract the contents of the downloaded file to a folder named “git”.

c) Create a new PHP script file and save it with a.php extension.

3. Create a new file to upload to the server

a) Create a new text file named “upload.php” and save it in the “php” folder.

b) Save this file as a PHP file with a.php extension.

4. Upload the archive.tar.gz to the server

a) Log in to your PHP web server (e.g. Apache) as the administrator and navigate to the “Uploads” directory.

b) Open the archive.tar.gz file in a text editor or the web interface.

c) Open the “upload.php” file in your web browser.

5. Upload the file to the server

a) Log in to your web server (e.g. Nginx, Apache, IIS) as the administrator.

b) Open the “upload.php” file in your web browser.

c) Upload the archive.tar.gz file to the desired location on the server.

6. Display a success message on the webpage

a) Add the following code at the beginning of your “upload.php” file to display a success message:

```
header('Content-type: text/html; charset=utf-8');
exit('<p>File uploaded successfully</p>');
```

b) Save this code as a PHP file with a.php extension.

7. Remove the extracted directory

a) Log in to your PHP web server (e.g. Apache) as the administrator and navigate to the “extracted” directory.

b) Delete the extracted
```

**Fine-Tuned Model Output:**
```
1. Extract the contents of archive.tar.gz to extracted.
2. Verify that the contents of extracted folder are a directory.
3. Create a file in extracted folder named index.html.
4. Replace the contents of index.html with the updated index.html file.
5. Create a directory named fonts and move the files from fonts.zip to the extracted folder.
6. Create a directory named css and move the files from css.zip to the extracted folder.
7. Run npm install and npm start.

Step 8: Installation

1. In your command prompt, navigate to the extracted folder and run npm install. This will download the updated index.html, fonts, and css files from npm.
2. Run npm start and open the file index.html in your web browser.

That’s it! You’ve successfully deployed an updated version of your React application to AWS Lambda using NPM and AWS Amplify.
```

**BLEU Score:** `0.0354`

**ROUGE-L Score:** `0.2107`

---

