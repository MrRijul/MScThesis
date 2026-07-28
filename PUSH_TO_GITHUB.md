# Push this repository to GitHub

## 1. Open this folder in VS Code

Open the extracted `deposit-franchise-value` folder, not your original thesis working folder.

## 2. Initialise Git

```powershell
git init
git branch -M main
git status
```

## 3. Configure your identity if this is your first Git repository

```powershell
git config --global user.name "Rijul Sharma"
git config --global user.email "rijulsharmabusiness@gmail.com"
```

## 4. Stage only the public files

```powershell
git add .gitignore
git add README.md
git add requirements.txt
git add data/README.md
git add data/processed/.gitkeep
git add notebooks/01_empirical_analysis.ipynb
git add docs/.gitkeep
git add outputs/figures/.gitkeep
git status
```

Check that no `.csv`, `.xlsx`, `.parquet`, raw-data folder or bulk output folder appears under “Changes to be committed”.

## 5. Commit

```powershell
git commit -m "Publish MSc thesis analysis"
```

## 6. Create the empty GitHub repository

Create a public repository named:

```text
deposit-franchise-value
```

Do not pre-create a README, `.gitignore` or licence on GitHub.

## 7. Connect and push

Replace `YOUR_GITHUB_USERNAME`:

```powershell
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/deposit-franchise-value.git
git remote -v
git push -u origin main
```

## 8. Add the overview later

Export the condensed thesis overview as:

```text
docs/thesis_overview.pdf
```

Add two or three selected PNG figures to `outputs/figures/`, then run:

```powershell
git add docs/thesis_overview.pdf
git add outputs/figures/
git status
git commit -m "Add thesis overview and selected results"
git push
```
