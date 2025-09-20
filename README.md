# Daily Planner

A GitHub-based daily planner system that automatically creates daily planning issues and provides easy access to them through a simple web interface.

## How it works

This system uses GitHub Issues, GitHub Actions, and GitHub Pages to create a seamless daily planning experience:

1. **Issue Template**: Provides a structured template for daily planning with sections for priorities, tasks, and notes
2. **Auto-redirect Page**: A webpage that either redirects you to today's existing issue or creates a new one
3. **GitHub Actions**: Automatically updates the issue index when new issues are created
4. **GitHub Pages**: Hosts the redirect page so you can bookmark it or set it as your homepage

## Setup Instructions

1. **Create a GitHub repository** for your daily planner (can be private or public)

2. **Update the repository URL** in `index.html`:
   - Find line 65: `const repoUrl = 'YOUR_USERNAME/YOUR_REPO';`
   - Replace with your actual GitHub username and repository name
   - Example: `const repoUrl = 'johndoe/daily-planner';`

3. **Initialize and push to GitHub**:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git push -u origin main
   ```

4. **Enable GitHub Pages**:
   - Go to your repository on GitHub
   - Navigate to Settings → Pages
   - Set Source to "Deploy from a branch"
   - Select "main" branch and "/ (root)" folder
   - Save

5. **Test the workflow**:
   - Visit your GitHub Pages URL (usually `https://YOUR_USERNAME.github.io/YOUR_REPO/`)
   - It should redirect you to create a new daily issue or show today's existing issue

## Usage

- **Bookmark** your GitHub Pages URL or set it as your browser homepage
- **Visit the page** each day to access your daily planner
- **The system will automatically**:
  - Create a new issue for today if none exists
  - Redirect you to today's existing issue if it's already created
  - Update the issue index whenever new issues are opened

## File Structure

```
.
├── index.html                          # Main redirector page
├── issue-titles.json                   # Auto-generated issue index
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── day.yml                     # Daily planner issue template
│   └── workflows/
│       └── issues.yml                  # GitHub Actions workflow
└── README.md                           # This file
```

## Customization

- **Issue Template**: Modify `.github/ISSUE_TEMPLATE/day.yml` to change the fields in your daily issues
- **Styling**: Update the CSS in `index.html` to customize the look of the redirector page
- **Date Format**: Change the date formatting logic in `index.html` to match your preferences

## Inspired By

This project is based on Simon Willison's daily planner system described in his TIL: [GitHub Actions, Issues and Pages to build a daily planner](https://til.simonwillison.net/github-actions/daily-planner).