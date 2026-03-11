# Prompt Log

---

## Prompt 1

**Tool:** Copilot PRO

1. **Context** - The dataframe display in the notebook looked plain and had minor typos. I wanted a more polished, readable presentation for submission.
2. **Prompt(s)** - "Make the current dataframe more professional looking, and correct any typos or mistakes."
3. **Relevant Output** - Copilot inspected the active notebook cell and replaced the display code with a pandas Styler block using background gradients and formatted column headers.
4. **Validation** - Ran the cell and visually confirmed the table rendered with styling applied. Also checked that Jinja2 was importable after installation by running `import jinja2; print(jinja2.__version__)` in the notebook.
5. **Adaptations** - The default color scheme did not match the notebook visual style. Manually changed the gradient colors and re-imported Jinja2 explicitly after it was flagged as missing.
6. **Final Decision** - **Partially used.** Core styling structure was kept; color palette and some formatting details were changed manually.

---

## Prompt 2

**Tool:** Copilot PRO

1. **Context** - The assignment required a README.MD with six mandatory sections. The file was empty and needed a complete scaffold to fill in.
2. **Prompt(s)** - "Generate me the structure of a readme file so that I can fill it in with my own data." (Assignment section requirements copy-pasted in full as context.)
3. **Relevant Output** - Copilot generated a full README.MD template with all six required sections and placeholder text, then ran system commands to auto-fill OS version, Python version, pip version, GitHub username, and date.
4. **Validation** - Compared every generated section against the assignment rubric line by line. Verified that system values (Python 3.14.2, pip 25.3, Windows 11 10.0.26200) matched actual terminal output from `python --version` and `pip --version`.
5. **Adaptations** - Replaced the generic project path placeholder with the actual path. Removed the conda section since conda is not installed. Filled in the full name manually.
6. **Final Decision** - **Partially used.** Structure and auto-filled system values accepted; personal fields, expected outputs, problems encountered and wording adjusted manually.

---

## Prompt 3

**Tool:** Copilot PRO

1. **Context** - The repository needed a .gitignore to prevent committing notebook checkpoints, Python cache files, and FastF1 data caches.
2. **Prompt(s)** - "I would like a .gitignore file for this folder. It should include at minimum: data caches, __pycache__, .ipynb_checkpoints."
3. **Relevant Output** - Copilot checked whether a .gitignore already existed, then created one covering __pycache__/, .ipynb_checkpoints/, .cache/, *_cache/, and data/fastf1_cache/.
4. **Validation** - Ran `git status` after adding a test cache folder and confirmed it did not appear as an untracked file. Verified .ipynb_checkpoints was suppressed after opening and saving a notebook.
5. **Adaptations** - None required; the generated patterns covered all necessary cases.
6. **Final Decision** - **Used.** Output was correct and complete with no modifications needed.

---

## Prompt 4

**Tool:** Copilot PRO

1. **Context** - The existing PROMPTS.md used a flat table format that did not meet the assignment's required six-field structure for prompt documentation.
2. **Prompt(s)** - "Adapt prompts to use the six field format: 1. Context, 2. Prompt(s), 3. Relevant Output, 4. Validation, 5. Adaptations, 6. Final Decision."
3. **Relevant Output** - Copilot rewrote all three existing prompt entries from a Markdown table into individually sectioned entries each containing all six required fields with appropriate content drawn from the original entries.
4. **Validation** - Read the final file back and confirmed all three prompts contained each of the six numbered fields with non-placeholder content. Cross-checked field labels against the assignment specification.
5. **Adaptations** - None; the generated structure matched the required format exactly.
6. **Final Decision** - **Used.** Output matched the required format and content was accurate.
