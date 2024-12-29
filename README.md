# Hugo Installation and Setup Guide

This guide will walk you through installing Hugo, creating a new Hugo site, and setting it up with the PaperMod theme. We'll also cover basic hosting and deployment.

## 1. Install Go
Hugo requires Go for installation. Follow these steps:

### Step 1: Download Go
Visit the official Go download page:
[https://go.dev/dl/](https://go.dev/dl/)

### Step 2: Install Go
- For Windows, download the `.msi` file and run the installer.
- Follow the on-screen instructions to complete the installation.
- Add Go to your system's PATH environment variable if not automatically configured.

### Step 3: Verify Go Installation
Open your terminal and run:
```bash
go version
```
You should see the installed version of Go.

## 2. Install Hugo

### Step 1: Download Hugo
Visit the Hugo installation page:
[https://gohugo.io/installation/windows/](https://gohugo.io/installation/windows/)

Download the **Hugo extended version** (`.zip`) for Windows.

### Step 2: Extract and Configure Hugo
- Extract the downloaded `.zip` file.
- Move the `hugo.exe` file to a directory included in your system's PATH (e.g., `C:\Program Files\Hugo`).

### Step 3: Verify Hugo Installation
Run the following command in your terminal:
```bash
hugo version
```
Ensure that it shows the extended version (e.g., `Hugo Static Site Generator v0.140.1/extended`).

## 3. Create a New Hugo Site

### Step 1: Initialize a New Site
Run the following command:
```bash
hugo new site quickstart
```
This creates a new Hugo site in the `quickstart` directory.

### Step 2: Add a Theme
We'll use the Hugo PaperMod theme. Follow these steps:

1. Navigate to your new site's directory:
   ```bash
   cd quickstart
   ```
2. Clone the PaperMod theme:
   ```bash
   git init
   git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/hugo-papermod
   ```
3. Configure the theme in `config.toml`:
   ```toml
   theme = "hugo-papermod"
   ```

### Step 3: Add Example Content
Create a new post:
```bash
hugo new posts/my-first-post.md
```
Edit the newly created file in `content/posts/my-first-post.md` and add some content.

### Step 4: Start the Hugo Server
Run the development server:
```bash
hugo server -D
```
Visit `http://localhost:1313` in your browser to view your site.

## 4. Deploy Your Site

### Step 1: Build the Site
Run the following command to generate the static files:
```bash
hugo -D
```
The generated files will be in the `public` directory.

### Step 2: Choose a Hosting Provider
- **GitHub Pages**: [Host on GitHub Pages](https://gohugo.io/hosting-and-deployment/hosting-on-github/)
- **Netlify**: [Deploy on Netlify](https://gohugo.io/hosting-and-deployment/hosting-on-netlify/)
- **Vercel**: [Deploy on Vercel](https://gohugo.io/hosting-and-deployment/hosting-on-vercel/)

### Step 3: Deploy the Site
Follow the hosting provider's instructions to upload the `public` directory and make your site live.

## 5. Resources
- [Hugo Documentation](https://gohugo.io/documentation/)
- [Themes Directory](https://themes.gohugo.io/)
- [PaperMod Theme Documentation](https://github.com/adityatelange/hugo-PaperMod)
- [Hugo Hosting and Deployment](https://gohugo.io/hosting-and-deployment/)

Enjoy building your site with Hugo!