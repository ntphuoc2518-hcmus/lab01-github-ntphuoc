# Study Assistant — starter

A starter repository for the CSC10014 Smart Virtual Assistant project.

## Setup

1. Clone the repository:

    Clone the repository and enter the project directory:
   ```powershell
   git clone https://github.com/ntphuoc2518-hcmus/lab01-github-ntphuoc.git
   cd lab01-github-ntphuoc

2. Create a Python virtual environmentL:

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
4 passed
```

## Project structure

- `data/` — contains data files used by the project.
- `docs/` — contains project documentation.
- `scripts/` — contains utility and environment-checking scripts.
- `src/` — contains the main source code of the project.
- `tests/` — contains automated tests.
- `ui/` — contains files related to the user interface.
