# How to Update Your Website

This guide will help you update different sections of your website, add images, and commit your changes.

## Table of Contents
1. [Modifying Text Content](#modifying-text-content)
2. [Adding Images](#adding-images)
3. [Managing Publications](#managing-publications)
4. [Updating Site Configuration](#updating-site-configuration)
5. [Modifying Navigation Menu](#modifying-navigation-menu)
6. [Adding Blog Posts](#adding-blog-posts)
7. [Committing and Pushing Changes](#committing-and-pushing-changes)

---

## Modifying Text Content

### Homepage / About Page
**File:** `_pages/about.md`

This is your main landing page. Edit the content after the front matter (the section between `---` markers at the top).

- **Title**: Change `title: "Pierrot Lamontagne"` in the front matter
- **Main content**: Edit the text below the front matter
- **Contact section**: Modify the email addresses and links
- **Documents section**: Update file paths if you add new PDFs

**Example:**
```markdown
---
permalink: /
title: "Pierrot Lamontagne"
author_profile: true
---

Your main bio text goes here...
```

### Research Page
**File:** `_pages/research.md`

Edit this file to update your research description, current projects, and research themes.

- **Main description**: Edit the introductory paragraph
- **Sections**: Modify or add sections using `======` headers
- **Project descriptions**: Update the content under each section

### Outreach Page
**File:** `_pages/outreach.md`

Edit this file to add or update your outreach activities and content.

### Other Pages
- **Talks**: `_pages/talks.html` or `_talks/` folder
- **Teaching**: `_pages/teaching.html` or `_teaching/` folder
- **Portfolio**: `_pages/portfolio.html` or `_portfolio/` folder

---

## Adding Images

### Step 1: Place Your Image File
1. Add your image file to the `images/` folder
2. Supported formats: `.jpg`, `.jpeg`, `.png`, `.gif`, `.svg`
3. Use descriptive filenames (e.g., `conference_2024.jpg`)

### Step 2: Reference the Image in Markdown
In any `.md` file, use this syntax:

```markdown
![Alt text description](/images/your-image-name.jpg)
```

**Example from your about page:**
```markdown
![IAA-CSIC logo](/images/IAA-CSIC_logo.png)
![Observing for NIRPS at La Silla](/images/me_at_la_silla.jpg)
```

### Step 3: Profile Picture
To update your profile picture (shown in the sidebar):
1. Place the image in the `images/` folder
2. Update `_config.yml`:
   ```yaml
   author:
     avatar: "your-profile-picture.jpg"
   ```

### Image Best Practices
- **Optimize images**: Use compressed images to keep page load times fast
- **Descriptive alt text**: Always include meaningful alt text for accessibility
- **Consistent sizing**: Consider resizing images before uploading (recommended width: 800-1200px for content images)

---

## Managing Publications

### Adding a New Publication

**File location:** `_publications/`

**File naming format:** `YYYY-MM-DD-publication-title.md`

**Example filename:** `2025-01-15-my-new-paper.md`

### Publication File Structure

Create a new file in `_publications/` with this structure:

```markdown
---
title: "Your Paper Title"
collection: publications
permalink: /publication/YYYY-MM-DD-short-title
date: YYYY-MM-DD
venue: 'Journal Name or Conference Name'
paperurl: 'https://arxiv.org/abs/XXXX.XXXXX'
citation: 'Your citation here'
---

[Access paper here](https://arxiv.org/abs/XXXX.XXXXX){:target="_blank"}
```

### Required Fields
- **title**: Full title of the publication
- **collection**: Always `publications`
- **permalink**: URL-friendly version (use hyphens, lowercase)
- **date**: Publication date (YYYY-MM-DD format)
- **venue**: Journal name, conference name, or "Manuscript" for preprints
- **paperurl**: Link to paper (arXiv, journal, etc.)
- **citation**: Full citation text

### Example Publication Entry

```markdown
---
title: "NIRPS tightens the mass estimate of GJ 3090 b"
collection: publications
permalink: /publication/2026-01-01-nirps-gj3090
date: 2026-01-01
venue: 'Astrophysical Journal'
paperurl: 'https://arxiv.org/abs/2601.09330'
citation: 'Lamontagne, P., et al. "NIRPS tightens the mass estimate of GJ 3090 b." ApJ, 2026.'
---

[Access paper here](https://arxiv.org/abs/2601.09330){:target="_blank"}
```

### Editing Existing Publications
Simply open the file in `_publications/` and edit the content. Publications are automatically sorted by date (newest first) on the publications page.

### Removing Publications
Delete the corresponding `.md` file from `_publications/` folder.

---

## Updating Site Configuration

**File:** `_config.yml`

This file controls site-wide settings. **Important:** After editing `_config.yml`, you must restart Jekyll if running locally.

### Author Information
Update your personal information in the `author:` section:

```yaml
author:
  avatar: "profile.jpg"
  name: "Pierrot Lamontagne"
  bio: "Your bio text here"
  location: "Granada, Spain"
  employer: "IAA-CSIC"
  email: "your.email@example.com"
  # Add or update social media links
  github: "pierrotlamontagne"
  linkedin: "pierrot-lamontagne-68a2611b9"
  googlescholar: "https://scholar.google.com/..."
```

### Site Title and Description
```yaml
title: "Pierrot Lamontagne | Exoplanet Research"
description: "Your site description here"
```

### Site Theme
Change the theme by modifying:
```yaml
site_theme: "contrast"  # Options: "default", "air", "sunrise", "mint", "dirt", "contrast"
```

### Site URL
```yaml
url: https://pierrotlamontagne.github.io
```

---

## Modifying Navigation Menu

**File:** `_data/navigation.yml`

This file controls the header navigation menu.

### Current Menu Structure
```yaml
main:
  - title: "About"
    url: /
  - title: "Research"
    url: /research/
  - title: "Publications"
    url: /publications/
  - title: "Talks"
    url: /talks/
  - title: "Outreach"
    url: /outreach/
```

### Adding a New Menu Item
1. Add a new entry to the `main:` list
2. Create the corresponding page in `_pages/` if it doesn't exist
3. Use the format:
   ```yaml
   - title: "Page Title"
     url: /page-url/
   ```

### Reordering Menu Items
Simply reorder the items in the `main:` list. The order in the file determines the order in the navigation bar.

### Removing Menu Items
Delete the entry from `navigation.yml`. Note: This removes it from the menu but doesn't delete the page itself.

---

## Adding Blog Posts

**File location:** `_posts/`

**File naming format:** `YYYY-MM-DD-post-title.md`

### Blog Post Structure

```markdown
---
layout: single
title: "Your Post Title"
date: YYYY-MM-DD
categories:
  - category-name
tags:
  - tag1
  - tag2
author_profile: true
---

Your post content here...
```

### Example Blog Post

```markdown
---
layout: single
title: "My Conference Experience"
date: 2025-02-04
categories:
  - conferences
tags:
  - astronomy
  - exoplanets
author_profile: true
---

I recently attended the Exoplanet Conference...
```

---

## Adding Files (PDFs, Documents)

**Folder:** `files/`

1. Place your file (PDF, ZIP, etc.) in the `files/` folder
2. Reference it in your pages using:
   ```markdown
   [Download PDF](/files/your-file.pdf)
   ```

**Example from your about page:**
```markdown
* [Academic CV](/files/Academic_CV.pdf)
* [Publication list](/files/Publication%20list.pdf)
```

**Note:** If your filename has spaces, use `%20` for spaces in URLs, or rename the file to use hyphens/underscores.

---

## Committing and Pushing Changes

### Prerequisites
- Git must be installed
- You should have write access to the repository

### Step-by-Step Process

#### 1. Check Your Changes
Before committing, see what files have been modified:

```bash
git status
```

This shows:
- Modified files (in red)
- New files (in red, marked as "untracked")
- Files ready to commit (in green, marked as "staged")

#### 2. Stage Your Changes
Add specific files:
```bash
git add _pages/about.md
git add images/new-image.jpg
```

Or add all changes at once:
```bash
git add .
```

**Note:** Be careful with `git add .` - it stages ALL changes. Review with `git status` first.

#### 3. Commit Your Changes
Create a commit with a descriptive message:

```bash
git commit -m "Update about page with new research description"
```

**Good commit messages:**
- "Add new publication: GJ 3090 paper"
- "Update profile picture and bio"
- "Add conference talk to talks page"
- "Fix typo in research section"

**Bad commit messages:**
- "Update"
- "Changes"
- "Fix"

#### 4. Push to GitHub
Push your changes to the remote repository:

```bash
git push
```

If this is your first push or you're on a new branch, you might need:
```bash
git push origin main
```
(or `git push origin master` depending on your default branch name)

#### 5. Verify Your Changes
1. Go to your GitHub repository: `https://github.com/pierrotlamontagne/pierrotlamontagne.github.io`
2. Check that your commits appear in the history
3. Wait a few minutes for GitHub Pages to rebuild (usually 1-3 minutes)
4. Visit your website: `https://pierrotlamontagne.github.io`
5. Refresh the page to see your changes

### Complete Workflow Example

```bash
# 1. Make your edits to files (e.g., edit _pages/about.md)

# 2. Check what changed
git status

# 3. Stage the changes
git add _pages/about.md

# 4. Commit
git commit -m "Update bio with new research focus"

# 5. Push
git push

# 6. Wait 1-3 minutes, then check your website
```

### Troubleshooting

**If `git push` fails:**
- Make sure you're authenticated with GitHub
- Check if you have the latest changes: `git pull` first, then `git push`

**If changes don't appear on the website:**
- Check GitHub Actions/Pages build status in your repository
- Wait a few more minutes (builds can take 1-5 minutes)
- Hard refresh your browser (Ctrl+F5 or Cmd+Shift+R)
- Check for build errors in the GitHub Actions tab

**If you see merge conflicts:**
```bash
git pull
# Resolve conflicts in the files
git add .
git commit -m "Resolve merge conflicts"
git push
```

---

## Quick Reference

| What to Change | File Location |
|----------------|---------------|
| Homepage content | `_pages/about.md` |
| Research description | `_pages/research.md` |
| Outreach content | `_pages/outreach.md` |
| Add publication | `_publications/YYYY-MM-DD-title.md` |
| Add image | `images/` folder, then reference in markdown |
| Profile picture | `images/` folder + update `_config.yml` |
| Site title/description | `_config.yml` |
| Author info | `_config.yml` (author section) |
| Navigation menu | `_data/navigation.yml` |
| Add PDF/document | `files/` folder, then link in markdown |
| Add blog post | `_posts/YYYY-MM-DD-title.md` |

---

## Tips and Best Practices

1. **Test Locally First** (Optional but Recommended)
   - Install Jekyll locally (see README.md)
   - Run `bundle exec jekyll serve -l -H localhost`
   - Preview at `http://localhost:4000`
   - This lets you see changes before pushing

2. **Use Descriptive Commit Messages**
   - Future you will thank present you
   - Makes it easier to track changes

3. **Keep Images Optimized**
   - Large images slow down your site
   - Use image compression tools before uploading

4. **Regular Backups**
   - Your repository is already backed up on GitHub
   - Consider keeping local copies of important files

5. **Markdown Syntax**
   - Use `**bold**` for bold text
   - Use `*italic*` for italic text
   - Use `[link text](URL)` for links
   - Use `# Header` for headings

---

## Getting Help

- **Jekyll Documentation**: https://jekyllrb.com/docs/
- **Markdown Guide**: https://www.markdownguide.org/
- **GitHub Pages Docs**: https://docs.github.com/en/pages
- **Academic Pages Template**: https://academicpages.github.io/

---

**Last Updated:** February 2025
