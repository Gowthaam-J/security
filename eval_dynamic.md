# Dynamic Evaluation Report
**Note:** Manual scores (0–2) filled below each test case.

---

## Prompt 1:
**Input:**
```
Create a new Git branch and switch to it.
```

**Fine-Tuned Model Output:**
```
1. Switch to a new branch. This can be done using `git checkout -b my_new_branch_name`.
2. Make changes on the branch.
3. Commit and push the changes to the remote repository.
4. Switch back to the main branch using `git checkout main`.

I hope these tips and tricks help you get started with GitHub!
```

**Dry-Run Commands (Fine-Tuned):**
```bash
echo git checkout -b my_new_branch_name
echo git checkout main
```

**Manual Score:** `2`

---

## Prompt 2:
**Input:**
```
Compress the folder reports into reports.tar.gz
```

**Fine-Tuned Model Output:**
```
1. Open Terminal.
2. Run `tar -czvf reports.tar.gz reports` to compress the folder.
3. Verify the archive using `ls -lh` or inspect with `tar -tvf reports.tar.gz`.
4. Optionally, confirm the contents with:
   ```
   tar -xvzf reports.tar.gz -O | head
   ```
```

**Dry-Run Commands (Fine-Tuned):**
```bash
echo tar -czvf reports.tar.gz reports
echo ls -lh
```

**Manual Score:** `1`

---

## Prompt 3:
**Input:**
```
List all Python files in the current directory recursively.
```

**Fine-Tuned Model Output:**
```
1. Import the `os` module and create a new empty list named `file_list`.
2. Create a recursive function called `recursive_list_files`, which will be used to list Python files recursively.
3. Inside the function, use `os.walk()` to traverse directories.
4. Append files ending with `.py` to `file_list`.
5. Return and print the results.
```

**Example Usage:**
```python
import os

def recursive_list_files(path):
    file_list = []
    for root, dirs, files in os.walk(path):
        for file in files:
            if file.endswith(".py"):
                file_list.append(os.path.join(root, file))
    return file_list

if __name__ == '__main__':
    file_list = recursive_list_files('./')
    for f in file_list:
        print(f)
```

**Dry-Run Commands (Fine-Tuned):**
```bash
echo python list_python_files.py
```

**Manual Score:** `2`

---

## Prompt 4:
**Input:**
```
Set up a virtual environment and install requests.
```

**Fine-Tuned Model Output:**
```
1. Open terminal or command prompt.
2. Navigate to your project directory.
3. Create a virtual environment:
   ```
   python3 -m venv venv
   ```
4. Activate the environment:
   - Unix/macOS:
     ```
     source venv/bin/activate
     ```
   - Windows:
     ```
     venv\Scripts\activate
     ```
5. Install requests:
   ```
   pip install requests
   ```
6. Test with:
   ```python
   from requests import get
   r = get('https://www.google.com')
   print(r.text)
   ```
```

**Dry-Run Commands (Fine-Tuned):**
```bash
echo python3 -m venv venv
echo source venv/bin/activate
echo pip install requests
echo python python_test_requests.py
```

**Manual Score:** `2`

---

## Prompt 5:
**Input:**
```
Fetch only the first ten lines of a file named output.log.
```

**Fine-Tuned Model Output:**
```
1. Open terminal and navigate to the directory.
2. Use the command:
   ```
   head -n 10 output.log
   ```
3. Optionally save output:
   ```
   head -n 10 output.log > first_10_lines.txt
   ```
```

**Dry-Run Commands (Fine-Tuned):**
```bash
echo head -n 10 output.log
echo head -n 10 output.log > first_10_lines.txt
```

**Manual Score:** `2`

---

## Prompt 6:
**Input:**
```
Find and delete all .pyc files within the current directory and its subdirectories.
```

**Fine-Tuned Model Output:**
```
1. Open terminal and navigate to the project directory.
2. Run the following command:
   ```
   find . -name '*.pyc' -exec rm {} +
   ```
3. This deletes all `.pyc` files recursively.
```

**Dry-Run Commands (Fine-Tuned):**
```bash
echo find . -name '*.pyc' -exec rm {} +
```

**Manual Score:** `1`

---

## Prompt 7:
**Input:**
```
Extract the contents of archive.tar.gz to a folder named extracted, creating the folder if it doesn’t exist.
```

**Fine-Tuned Model Output:**
```
1. Open terminal or command prompt.
2. Run:
   ```
   mkdir -p extracted
   tar -xvf archive.tar.gz -C extracted
   ```
3. Verify with:
   ```
   ls extracted/
   ```
4. (Optional) Remove the archive:
   ```
   rm archive.tar.gz
   ```
5. If applicable, install Python dependencies:
   ```
   pip install -r requirements.txt
   ```
6. Run the project:
   ```
   python main.py
   ```
```

**Dry-Run Commands (Fine-Tuned):**
```bash
echo mkdir -p extracted
echo tar -xvf archive.tar.gz -C extracted
echo ls extracted/
echo rm archive.tar.gz
echo pip install -r requirements.txt
echo python main.py
```

**Manual Score:** `2`

---