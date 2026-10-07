# Setup Failure Log

## Failure 1 — Deleted virtual environment

### What I broke

I intentionally deleted the `.venv` directory:

```powershell
Remove-Item -Recurse -Force .venv
```
After that, the project no longer had its Python virtual environment and the test environment was not available.

### Symptom

Running the tests failed because the virtual environment and its installed dependencies were missing.

### How I recovered

I opened README.md and followed the setup instructions:

```powershell 
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
pip install -e .
pytest -q
```

### Verification

The tests passed again:

```powershell
5 passed
```

I also ran:

```powershell
python scripts/check_env.py
```

and the environment checks passed.

### Lesson learned 

The README contains enough setup information to recreate the development environment after the virtual environment is deleted.


