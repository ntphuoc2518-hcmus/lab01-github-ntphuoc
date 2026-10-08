# Lab 1 homework — Break your setup, recover from the README

1. Break it on purpose (choose one): delete `.venv`; move the repo to another folder; uninstall pytest; clone into a new folder.
2. Recover using **only** your README.
3. Record:

| What I broke | Error message I saw | How I fixed it | README change needed? |
|---|---|---|---|
| Deleted the `.venv` directory | The virtual environment and its installed dependencies were missing, so the test environment was not available. | Recreated `.venv`, activated it, installed the requirements, installed the project with `pip install -e .`, and ran `pytest -q`. The tests passed with `5 passed`. | No |

Commit the README fix (if any) with a Conventional Commit message and paste the link here.