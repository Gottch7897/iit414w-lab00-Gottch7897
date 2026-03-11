# IIT414W Lab 00

## (a) Header
- Full Name: `Martín Gottschalk`
- GitHub Username: `Gottch7897`
- Course Code: `IIT414W`
- Date: `2026-03-11`

## (b) System Info
- Operating System (name + version): `Microsoft Windows 11 Home Single Language (10.0.26200)`
- Python Version: `Python 3.14.2`
- Package Manager Version:
  - `pip --version`: `pip 25.3`

## (c) Setup Instructions

### Option 1: Setup from `requirements.txt`
```bash
# 1) Open terminal in project root
cd c:\Users\your-file-directory

# 2) (Recommended) Create and activate virtual environment
python -m venv .venv

# Windows PowerShell
.\.venv\Scripts\Activate.ps1

# macOS/Linux
source .venv/bin/activate

# 3) Upgrade pip and install dependencies
python -m pip install --upgrade pip
pip install -r requirements.txt
```
### Verify Setup
```bash
python --version
pip --version
```

## (d) How To Run
Run notebooks in this order because `data_check.ipynb` depends on environment and package checks first.

### Required Run Order
1. `setup_check.ipynb`
2. `data_check.ipynb`

### Command Examples
```bash

# run notebook 1
python -m jupyter nbconvert --to notebook --execute --inplace setup_check.ipynb

# run notebook 2
python -m jupyter nbconvert --to notebook --execute --inplace data_check.ipynb
```

```bash
# OR launch Jupyter UI and run all cells in order manually
python -m notebook
```

Notes:
- Keep notebook order: `setup_check.ipynb` then `data_check.ipynb`.
- Internet access is required for FastF1 session loading and Jolpica API requests.

## (e) Problems Encountered
Documented issues from this environment and setup flow:

### Problem 1
- Issue: `conda --version` failed because conda was not recognized.
- Cause: Conda is not installed or not available in `PATH` on this machine.
- Fix: Used a virtual environment with `requirements.txt` instead:
	- `python -m venv .venv`
	- `.\.venv\Scripts\Activate.ps1`
	- `pip install -r requirements.txt`

### Problem 2
- Issue: No `environment.yml` was available, so conda-based setup instructions were not runnable.
- Cause: Repository currently provides dependency specification through `requirements.txt` only.
- Fix: Updated setup process to a pip/venv workflow and validated with:
	- `python --version`
	- `pip --version`
	- notebook execution commands in Section (d)

## (f) Expected Outputs
Successful run indicators:

- `setup_check.ipynb`:
	- Prints reproducibility header values (`Python`, `NumPy`, `Seed`).
	- Prints dependency status (either installs missing packages or reports all required packages already installed).
	- Prints a 6-row package/version table for `numpy`, `pandas`, `sklearn`, `matplotlib`, `seaborn`, and `fastf1`.
	- Prints working directory, FastF1 cache path, Git version, and recent commits.


- `data_check.ipynb`:
	- Loads the 2024 Bahrain race session through FastF1 and prints session metadata.
	- Prints result dimensions/column names and lap preview output.
	- API request to `https://api.jolpi.ca/ergast/f1/2024/driverstandings/` returns status code 200.
	- Prints number of standings records and first three driver standings entries.

---

## Submission Checklist
- [+] Header is fully filled out
- [+] System info includes exact versions
- [ ] Setup commands are complete and tested
- [ ] Notebook run order is stated clearly
- [+] At least 2 real problems + fixes documented
- [] Expected outputs are specific and match actual results
