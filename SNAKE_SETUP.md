# 🐍 Snake Animation Setup Guide

## Quick Setup (3 Steps)

### Step 1: Enable Workflow Permissions ✅

1. Go to your GitHub repository: `https://github.com/suyashagrahari/suyashagrahari`
2. Click on **Settings** → **Actions** → **General**
3. Scroll down to **Workflow permissions**
4. Select **"Read and write permissions"**
5. Check **"Allow GitHub Actions to create and approve pull requests"**
6. Click **Save**

### Step 2: Verify the Workflow File ✅

The `snake.yml` file is already in place at:
```
.github/workflows/snake.yml
```

Make sure it contains:
- Your GitHub username: `suyashagrahari`
- Proper permissions: `contents: write`
- Correct action: `Platane/snk/svg-only@v3`

### Step 3: Run the Workflow ✅

1. Go to **Actions** tab in your repository
2. Click on **"Generate Snake"** workflow
3. Click **"Run workflow"** button (top right)
4. Select branch: `main`
5. Click **"Run workflow"**

## What Happens Next? 🎯

1. **First Run**: The workflow will create an `output` branch automatically
2. **Generate SVG**: It creates two snake SVG files:
   - `github-contribution-grid-snake.svg` (light theme)
   - `github-contribution-grid-snake-dark.svg` (dark theme)
3. **Auto-Update**: The workflow runs every 12 hours automatically
4. **Manual Trigger**: You can run it manually anytime from Actions tab

## Verify It's Working ✅

After the workflow runs successfully:

1. Check the **Actions** tab - should show ✅ green checkmark
2. Go to **Branches** - you should see an `output` branch
3. Check the `output` branch - should contain the SVG files
4. Your README.md already has the snake image link - it should appear automatically!

## Troubleshooting 🔧

### Issue: Workflow fails with "Permission denied"
**Solution**: Make sure you completed Step 1 (Enable Workflow Permissions)

### Issue: Snake doesn't appear in README
**Solution**: 
- Wait 1-2 minutes after workflow completes
- Check if the `output` branch exists
- Verify the image URL in README.md matches: 
  ```
  https://raw.githubusercontent.com/suyashagrahari/suyashagrahari/output/github-contribution-grid-snake-dark.svg
  ```

### Issue: Workflow doesn't run automatically
**Solution**: 
- First run must be manual
- After that, it runs every 12 hours automatically
- You can always trigger it manually from Actions tab

### Issue: Snake shows old contributions
**Solution**: 
- The snake updates based on your GitHub contribution graph
- Make commits to see the snake grow!
- The animation updates every 12 hours

## Customization Options 🎨

### Change Update Frequency
Edit `snake.yml` and modify the cron schedule:
```yaml
schedule:
  - cron: "0 */6 * * *"  # Every 6 hours
  - cron: "0 0 * * *"    # Daily at midnight
```

### Use Light Theme Snake
In your README.md, change the image URL to:
```markdown
![Snake animation](https://raw.githubusercontent.com/suyashagrahari/suyashagrahari/output/github-contribution-grid-snake.svg)
```

### Custom Colors
You can customize the palette by modifying the `outputs` section in `snake.yml`

## Need Help? 🆘

- Check GitHub Actions logs in the **Actions** tab
- Visit the official repo: https://github.com/Platane/snk
- Make sure your repository is **public** (required for the snake to work)

## Success Checklist ✅

- [ ] Workflow permissions enabled
- [ ] `snake.yml` file exists in `.github/workflows/`
- [ ] Workflow runs successfully (green checkmark)
- [ ] `output` branch created
- [ ] Snake appears in README.md
- [ ] Snake updates automatically every 12 hours

---

**🎉 Once all checkboxes are done, your snake animation is live!**

The snake will automatically update based on your GitHub contributions, making your profile more engaging and showing your coding activity! 🚀

