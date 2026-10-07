# Study Assistant – starter

A starter repository for the CSC10014 Smart Virtual Assistant project.

The project provides a command-line study assistant that can receive a question from the user and return an appropriate response.

## Prerequisites

Before setting up the project, make sure you have:

- Python 3.10 or newer
- Git
- Windows PowerShell (for Windows users)

You can check your versions with:

```powershell
python --version
git --version
```

## Setup

1. Clone the repository:

    Clone the repository and enter the project directory:
   ```powershell
   git clone https://github.com/ntphuoc2518-hcmus/lab01-github-ntphuoc.git
   cd lab01-github-ntphuoc

2. Create a Python virtual environment:

    Create a Python virtual environment:
    ```powershell
    python -m venv .venv

3. Activate the virtual environment on Windows PowerShell:

    On Windows PowerShell:
    ```powershell
    .\.venv\Scripts\Activate.ps1
    ```

    After activation, (.venv) should appear at the beginning of the terminal prompt.

    For example:
    ```powershell
    (.venv) PS C:\Users\Admin\projects\csc10014\lab01-github-ntphuoc>
    ```

4. Install the project dependencies:

    Install the required Python packages:
    ```powershell 
    pip install -r requirements.txt
    ```

    Then install the project in editable mode:
    ```powershell
    pip install -e .
    ```

5. Run the starter application:

    Make sure the virtual environment is activated:
    ```powershell
    .\.venv\Scripts\Activate.ps1
    ```

    Run the study assistant with:
    ```powershell
    python -m assistant "where is the IT helpdesk?"
    ```

    The command should run successfully and display the assistant's response to the question.

6. Run the tests:
    Make sure the virtual environment is activated, then run:
    ```powershell
    pytest -q
    ```

    The tests should complete successfully without errors.

    A successful result should show that the tests have passed, for example:
    ```powershell
    4 passed
    ```

    The exact number of tests may change as the project is developed.

## Run

Activate the virtual environment first:

```powershell
.\.venv\Scripts\Activate.ps1
```

Then run the application:

```powershell
python -m assistant "where is the IT helpdesk?"
```

The expected output:
```powershell
IT Helpdesk: room E.005, open Mon-Fri 08:00-17:00.
```

## Test

Run 

```powershell
pytest -q
```

The expected result:

```powershell
5 passed
```

## Project structure

```text
lab01-github-ntphuoc/
├── data/
│   └── offices.csv
├── docs/
│   └── lab1/
├── scripts/
│   └── check_env.py
├── src/
│   └── assistant/
│       └── rules.py
├── tests/
│   └── test_smoke.py
├── ui/
├── .gitignore
├── README.md
├── pyproject.toml
└── requirements.txt
```

### Folder and file descriptions

- `data/` — contains data files used by the project.
- `docs/` — contains project documentation and lab materials.
- `scripts/` — contains utility and environment-checking scripts.
- `src/` — contains the main source code of the project.
- `tests/` — contains automated tests.
- `ui/` — contains files related to the user interface.
- `.gitignore` — specifies files and folders that Git should ignore.
- `README.md` — contains project information and usage instructions.
- `pyproject.toml` — contains Python project configuration.
- `requirements.txt` — lists the project's Python dependencies.

## Troubleshooting

### 1. Python command is not recognized

If `python` is not recognized, make sure Python 3.10 or newer is installed and added to PATH.

Check the Python version:

```powershell
python --version
```

### 2. Virtual environment cannot be activated on PowerShell

If PowerShell blocks the activation script, run:
```powershell 
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

Then activate the virtual environment again:
```powershell
.venv\Scripts\Activate.ps1
```
### 3. Dependencies are missing

If the program cannot import a required package, make sure the virtual environment is activated and install the dependencies:
```powershell
pip install -r requirements.txt
```

If the project package is not recognized, install it in editable mode:
```powershell
pip install -e .
```

### 4. Tests fail

Run the tests with:
```powershell
pytest -q
```
If a test fails, check that you are running the command from the project root directory and that the virtual environment is activated.

### 5. Git push is rejected with a 403 error
If you see:
```powershell
remote: Permission to ... denied
fatal: ... 403
```
make sure you are authenticated with the GitHub account that has permission to access the repository.

For HTTPS authentication, Git may ask you to complete authentication in your browser.

You can check the repository remote with:

```powershell
git remote -v
```