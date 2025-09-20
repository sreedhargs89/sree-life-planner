# GitHub Pages Setup Guide

## Current Status
✅ Repository created: `sreedhargs89/sree-life-planner`
✅ All files committed and pushed
✅ GitHub Actions workflow updated with proper Pages deployment
✅ Improved error handling and debugging in index.html

## Next Steps to Complete Setup

### 1. Enable GitHub Pages
1. Go to your repository: https://github.com/sreedhargs89/sree-life-planner
2. Click on **Settings** tab
3. Scroll down to **Pages** section in the left sidebar
4. Under **Source**, select **GitHub Actions** (not "Deploy from branch")
5. Save the settings

### 2. Check GitHub Actions Workflow
1. Go to the **Actions** tab in your repository
2. You should see a workflow run called "Generate Issues JSON and Deploy"
3. If it's failing, check the logs for any permission issues

### 3. Verify GitHub Pages Deployment
Once the workflow completes successfully:
- Your site will be available at: https://sreedhargs89.github.io/sree-life-planner/
- The workflow will automatically generate `issue-titles.json`
- The site should redirect you to create or view daily issues

### 4. Create Your First Daily Issue (Manual Test)
1. Go to: https://github.com/sreedhargs89/sree-life-planner/issues/new?template=day.yml
2. Create an issue with today's date
3. After creating the issue, the workflow should update `issue-titles.json` automatically

### 5. Test the Complete System
1. Visit your GitHub Pages site: https://sreedhargs89.github.io/sree-life-planner/
2. It should either:
   - Redirect to today's existing issue, OR
   - Take you to create a new issue for today

## Troubleshooting

### If GitHub Pages shows 404:
- Make sure Pages source is set to "GitHub Actions"
- Check that the workflow completed successfully
- Wait a few minutes after workflow completion

### If the workflow fails:
- Check the Actions tab for error logs
- Ensure repository has proper permissions
- The workflow needs `pages: write` and `id-token: write` permissions

### If issue-titles.json is not found:
- The workflow generates this file automatically
- Check the Actions tab to see if the workflow has run
- You can manually trigger it from the Actions tab

### If redirects don't work:
- Check browser developer console for errors
- The debug section on the page will show detailed information
- Use the "Create Issue Manually" link as a fallback

## Features

✨ **Automatic Daily Issues**: Creates structured daily planning issues
✨ **Smart Redirects**: Finds existing issues or creates new ones
✨ **GitHub Actions Integration**: Automatically updates issue index
✨ **Mobile Friendly**: Responsive design works on all devices
✨ **Debug Information**: Built-in troubleshooting tools
✨ **Fallback Links**: Manual issue creation if auto-redirect fails

## Usage Tips

1. **Bookmark the GitHub Pages URL** for daily access
2. **Set as homepage** for instant daily planning access  
3. **Use on mobile** - the interface is mobile-friendly
4. **Check the debug info** if something isn't working
5. **Create issues manually** using the fallback link if needed

Your daily planner system is now ready to use! 🚀