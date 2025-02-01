# Dockerfile Bug and Solution

This repository demonstrates a common error in Dockerfiles: failure to handle missing files and insufficient permissions. The original `Dockerfile` attempts to install dependencies and run a Python script but lacks necessary checks and permissions.  The `Dockerfile_fixed` provides a corrected version.

## Bug
The original Dockerfile causes an error because `requirements.txt` is not present in the build context, and `app.py` lacks executable permissions.

## Solution
The corrected Dockerfile includes explicit checks for file existence and sets the appropriate executable permissions for `app.py`. It also uses a more robust method of installing packages using a virtual environment.
