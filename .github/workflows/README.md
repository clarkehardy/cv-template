# GitHub Actions Setup Guide

This repository includes a GitHub Action that automatically builds your CV and deploys it to your website when you push changes.

## Setup Instructions

### 1. Enable the Workflow

The workflow is disabled by default. To enable it:

1. Edit `.github/workflows/deploy-to-website.yml`
2. Change `if: false` to `if: true` in the deploy job
3. Optionally, change the trigger from `workflow_dispatch` to `push` on your main branch

### 2. Set Up Deploy Key

You'll need to create a deploy key for your website repository:

1. Go to your website repository on GitHub
2. Navigate to Settings → Deploy keys
3. Click "Add deploy key"
4. Give it a title (e.g., "CV Deploy Key")
5. Copy the public key (you'll need this for step 3)
6. Check "Allow write access" if you want the action to push changes
7. Click "Add key"

### 3. Add Repository Secret

1. Go to this CV repository on GitHub
2. Navigate to Settings → Secrets and variables → Actions
3. Click "New repository secret"
4. Name: `WEBSITE_DEPLOY_KEY`
5. Value: Paste the **private** key from step 2
6. Click "Add secret"

### 4. Update Repository URLs

Edit `.github/workflows/deploy-to-website.yml` and replace:
- `YOUR_USERNAME` with your GitHub username
- `YOUR_WEBSITE_REPO` with your website repository name
- Update the file path in the "Clone website repo" step to match your website's structure

### 5. Test the Workflow

1. Make a small change to your CV
2. Commit and push to the main branch
3. Go to the Actions tab to see if the workflow runs successfully

## Troubleshooting

- **Permission denied**: Make sure the deploy key has write access to your website repository
- **Repository not found**: Double-check the repository URL in the workflow file
- **File not found**: Verify the file path in the "Clone website repo" step matches your website structure

## Customization

You can customize the workflow by:
- Changing the trigger conditions (e.g., only on specific branches)
- Modifying the LaTeX installation to include additional packages
- Adding additional build steps or file processing
- Changing the commit message format 