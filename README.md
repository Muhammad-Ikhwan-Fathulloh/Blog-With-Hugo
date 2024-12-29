# Hugo Installation and Setup Guide

This guide provides detailed steps to install Hugo, set up a project, and deploy it using various tools, including the PaperMod theme and Hextra documentation.

## Prerequisites

- Install Go (required for Hugo): [Download Go](https://go.dev/dl/)
- Basic knowledge of terminal/command-line usage.

## Step 1: Install Hugo

1. **Download Hugo**:
   - Visit the [Hugo installation page for Windows](https://gohugo.io/installation/windows/).
   - Download the appropriate version of Hugo (choose the **extended** version for SCSS/SASS support).

2. **Install Hugo**:
   - Extract the downloaded `.zip` file.
   - Move the `hugo.exe` file to a directory in your system `PATH` (e.g., `C:\Program Files\Hugo`).

3. **Verify Installation**:
   ```bash
   hugo version
   ```
   This should display the installed version of Hugo.

## Step 2: Create a New Hugo Site

1. **Initialize a New Project**:
   ```bash
   hugo new site quickstart
   ```

2. **Navigate to the Project Directory**:
   ```bash
   cd quickstart
   ```

## Step 3: Add a Theme

1. **Choose a Theme**:
   - Visit [Hugo Themes](https://themes.gohugo.io/) to explore available themes.

2. **Install the PaperMod Theme**:
   ```bash
   git init
   git submodule add https://github.com/adityatelange/hugo-PaperMod themes/PaperMod
   ```

3. **Configure the Theme**:
   - Open `hugo.toml` or `config.toml`.
   - Add the following line:
     ```toml
     theme = "PaperMod"
     ```

## Step 4: Create Content

1. **Add a New Page**:
   ```bash
   hugo new posts/my-first-post.md
   ```

2. **Edit the Page**:
   - Open `content/posts/my-first-post.md` in a text editor.
   - Add content and set the `draft` parameter to `false`.

## Step 5: Run the Development Server

Start the Hugo server to preview your site:
```bash
hugo server
```

Visit `http://localhost:1313` in your browser to see your site.

## Step 6: Deploy Your Site

1. **Build the Site**:
   ```bash
   hugo -D
   ```
   This generates the static site files in the `public/` directory.

2. **Deploy**:
   - Follow the [Hugo Hosting and Deployment Guide](https://gohugo.io/hosting-and-deployment/) for detailed instructions on deploying your site to various platforms, such as Netlify, GitHub Pages, or others.

## Step 7: Additional Features with Hextra

1. **Hextra Documentation**:
   - Explore advanced features and integrations using the [Hextra Documentation](https://imfing.github.io/hextra/docs/getting-started/).

2. **Hextra Setup**:
   - Follow the steps to enhance your Hugo site with Hextra's plugins and utilities for better documentation management.

---

### Resources

- [Go Installation](https://go.dev/dl/)
- [Hugo Official Documentation](https://gohugo.io/getting-started/quick-start/)
- [PaperMod Theme](https://themes.gohugo.io/themes/hugo-papermod/)
- [Hextra Documentation](https://imfing.github.io/hextra/docs/getting-started/)