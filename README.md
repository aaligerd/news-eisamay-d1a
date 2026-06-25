# News - Eisamay Website

This project is structured and optimized to be published as a static website on **GitHub Pages**.

## Reorganization & Path Fixes Done
To ensure that the website renders perfectly on GitHub Pages, the following improvements have been made:
1. **Homepage Named to `index.html`**: Renamed the main entry file from `news-eisamay.html` to `index.html`. GitHub Pages automatically serves `index.html` as the default landing page.
2. **Relative Link Conversion**: All hardcoded absolute links (e.g. `href="/"`) were updated to relative links (e.g. `href="index.html"`) so that the site links correctly when hosted under subpaths on GitHub Pages (e.g., `https://<username>.github.io/<repository-name>/`).
3. **Broken Mock Links Restructured**:
   - Navigation links pointing to non-existent `/category/...` or `/author/...` pages have been redirected to `news-listing.html` (which acts as a category/author list page).
   - Mock article links (e.g., `/urban/...`) have been linked to `news-details.html` (which acts as the article details page), making the entire prototype fully functional and browsable.
4. **CSS Path Fixes**: Converted domain-root paths (like `/static-images/...`) to relative paths (like `../static-images/...`) in `css/news-eisamay.css` so they resolve correctly relative to the stylesheet.
5. **Git Configuration**: Initialized a Git repository and added a standard `.gitignore` file.

---

## How to Publish to GitHub Pages

Follow these steps to host your website on GitHub Pages:

### Step 1: Create a Repository on GitHub
1. Open your web browser and go to [GitHub](https://github.com).
2. Log in to your account and click the **New** repository button (or go to `https://github.com/new`).
3. Name your repository (e.g., `news-eisamay-sb`).
4. Keep the repository **Public** (required for free GitHub Pages hosting).
5. **Do NOT** check "Add a README file", "Add .gitignore", or "Choose a license" (since we already have these files locally).
6. Click **Create repository**.

### Step 2: Push Your Local Code to GitHub
Open your terminal/command prompt in this project folder (`D:\news-eisamay-sb`) and run the following commands:

```bash
# 1. Add all project files
git add .

# 2. Create the first commit
git commit -m "Initial commit: prepare project structure for GitHub Pages"

# 3. Rename the default branch to main
git branch -M main

# 4. Link your local project to your GitHub repository
# Replace <YOUR-GITHUB-USERNAME> and <YOUR-REPO-NAME> with your actual details
git remote add origin https://github.com/<YOUR-GITHUB-USERNAME>/<YOUR-REPO-NAME>.git

# 5. Push your code to GitHub
git push -u origin main
```

*Note: GitHub will prompt you to authenticate if you haven't logged in via your CLI.*

### Step 3: Enable GitHub Pages
1. Go to your repository page on GitHub.
2. Click on the **Settings** tab (the gear icon at the top of the repository page).
3. In the left sidebar, click on **Pages** (under the "Code and automation" section).
4. Under **Build and deployment**:
   - Source: Select **Deploy from a branch**.
   - Branch: Select **main** from the dropdown menu and leave the folder as `/ (root)`.
5. Click the **Save** button.
6. Wait 1-2 minutes. Refresh the settings page, and you will see a banner at the top of the Pages section saying:
   > Your site is live at `https://<username>.github.io/<repository-name>/`

---

## File and Folder Structure

The project has the following clean layout:
- `index.html`: The home page of the website (renamed from `news-eisamay.html`).
- `news-listing.html`: The article category listing page.
- `news-details.html`: The individual news article detail page.
- `css/`: Folder containing styling:
  - `news-eisamay.css`: Custom page styles (with relative paths).
  - `mat.css`: Theme styles.
- `img/`: Folder containing local images and logos (referenced relatively).
- `.gitignore`: Configured to exclude operating system and editor cache files.
