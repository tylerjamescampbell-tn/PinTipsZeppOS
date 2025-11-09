# Contributing to PinTipsZeppOS

## How to Upload Your Project Files to This Repository

If you have PinTips project files on your PC and want to upload them to this repository, follow these steps:

### Prerequisites
- Git installed on your computer ([Download Git](https://git-scm.com/downloads))
- Your project files organized on your PC
- GitHub account with access to this repository

### Step-by-Step Guide

#### 1. Clone the Repository
Open your terminal/command prompt and run:
```bash
git clone https://github.com/tylerjamescampbell-tn/PinTipsZeppOS.git
cd PinTipsZeppOS
```

#### 2. Create a New Branch
It's best practice to work on a new branch:
```bash
git checkout -b add-project-files
```

#### 3. Copy Your Files
Copy your project files from your PC into the cloned repository directory.

**Where to copy:** After running the commands above, you'll be in the `PinTipsZeppOS` directory. This is where you copy your files.

**How to find the location:**
- **Command Line:** Run `pwd` (Mac/Linux) or `cd` (Windows) to see the full path
- **File Explorer:** Navigate to the location where you cloned the repo

Copy all your project files into this directory. Typical ZeppOS project structure might include:
```
PinTipsZeppOS/
├── app.js                  # Main application file
├── app.json                # App configuration
├── assets/                 # Images, icons, fonts
├── pages/                  # Page files
├── utils/                  # Utility functions
└── package.json            # Dependencies (if any)
```

#### 4. Check What Files Will Be Added
```bash
git status
```
This shows all new files that will be added.

#### 5. Add Your Files to Git
```bash
git add .
```
Or add specific files:
```bash
git add app.js app.json
git add assets/
```

#### 6. Commit Your Changes
```bash
git commit -m "Add PinTips ZeppOS project files"
```

#### 7. Push to GitHub
```bash
git push origin add-project-files
```

#### 8. Create a Pull Request
1. Go to https://github.com/tylerjamescampbell-tn/PinTipsZeppOS
2. Click "Pull requests" > "New pull request"
3. Select your branch (`add-project-files`)
4. Add a description of what you're uploading
5. Click "Create pull request"

### Alternative: Using GitHub Desktop
1. Download [GitHub Desktop](https://desktop.github.com/)
2. Clone the repository through the app
3. Copy your files into the repository folder
4. In GitHub Desktop, you'll see all changes
5. Add a commit message and click "Commit"
6. Click "Push origin" to upload

### Alternative: Upload via GitHub Web Interface
For small projects, you can upload files directly through GitHub:
1. Go to https://github.com/tylerjamescampbell-tn/PinTipsZeppOS
2. Click "Add file" > "Upload files"
3. Drag and drop your files
4. Add a commit message
5. Choose "Create a new branch" and start a pull request
6. Click "Propose changes"

### What Files to Include
✅ **Include:**
- Source code (`.js`, `.json`)
- Assets (images, fonts, icons)
- Configuration files
- Documentation (README, guides)
- Build configuration

❌ **Don't Include:**
- `node_modules/` directory (use package.json instead)
- Build output directories
- IDE-specific files (`.vscode/`, `.idea/`)
- OS files (`.DS_Store`, `Thumbs.db`)
- Sensitive data (API keys, passwords)

### Need Help?
- Check the [GitHub Documentation](https://docs.github.com/)
- Ask questions in Issues
- Review ZeppOS documentation for project structure

## ZeppOS Project Structure

For a typical ZeppOS project, your structure might look like:

```
PinTipsZeppOS/
├── app.json                # App configuration and metadata
├── app.js                  # App lifecycle management
├── page/                   # App pages
│   └── index.js           # Main page logic
├── assets/                 # Static resources
│   ├── images/            # Images and icons
│   └── fonts/             # Custom fonts
└── utils/                  # Utility functions and helpers
```

Refer to the [ZeppOS Developer Documentation](https://docs.zepp.com/docs/intro/) for more details.
