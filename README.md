# Kocsis David - Portfolio Website

This is the source code for my personal portfolio website hosted at [kocsis-david.github.io](https://kocsis-david.github.io).

Website template based on [Jon Barron's design](https://github.com/jonbarron/jonbarron_website).

## 📋 Table of Contents

- [Quick Start](#quick-start)
- [How to Update Your Profile Image](#how-to-update-your-profile-image)
- [How to Update Project Descriptions](#how-to-update-project-descriptions)
- [How to Add Project Images](#how-to-add-project-images)
- [How to Add a New Project](#how-to-add-a-new-project)
- [How to Add Papers/Publications](#how-to-add-paperspublications)
- [File Structure](#file-structure)
- [Deployment](#deployment)

## 🚀 Quick Start

This is a static HTML website. To view it locally:

1. Clone the repository
2. Open `index.html` in your web browser

No build process or dependencies required!

## 🖼️ How to Update Your Profile Image

### Option 1: Replace the existing image
1. Prepare your profile photo (recommended: square, at least 400x400px)
2. Name it `JonBarron.jpg` (or any name you prefer)
3. Place it in the `images/` directory
4. If you used a different name, update line 31 in `index.html`:
   ```html
   <img style="width:100%;max-width:100%;object-fit: cover; border-radius: 50%;" 
        alt="profile photo" src="images/YOUR_IMAGE_NAME.jpg" class="hoverZoomLink">
   ```

### Option 2: Use a different image format
- Supported formats: `.jpg`, `.png`, `.webp`
- Make sure to update the file extension in `index.html`

## ✏️ How to Update Project Descriptions

Project information is stored in `index.html` between lines 47-222. Each project follows this structure:

```html
<tr>
  <td style="padding:16px;width:20%;vertical-align:middle">
    <img src='images/PROJECT_IMAGE.jpg' width=100%>
  </td>
  <td style="padding:8px;width:80%;vertical-align:middle">
    <a href="GITHUB_LINK">
      <span class="papertitle">Project Title</span>
    </a>
    <br>
    <em>Technology/Language</em>, Year
    <br>
    <a href="GITHUB_LINK">GitHub</a>
    <p></p>
    <p>
      Project description goes here.
    </p>
  </td>
</tr>
```

### To update a project description:
1. Open `index.html`
2. Find the project you want to update (search for the project title)
3. Modify the text between `<p>` and `</p>` tags
4. Save the file

### To update project details:
- **Title**: Change text in `<span class="papertitle">...</span>`
- **Technology**: Change text in `<em>...</em>`
- **Year**: Update the year after the technology
- **Link**: Update the `href` attribute in the `<a>` tags

## 🎨 How to Add Project Images

Currently, all projects use the same placeholder image (`JonBarron.jpg`). To add unique images for each project:

### Step 1: Prepare your images
1. Create or find an image that represents your project
2. Recommended size: 400x300px or similar aspect ratio
3. Supported formats: `.jpg`, `.png`, `.webp`, `.gif`, `.mp4` (for animations)

### Step 2: Add the image to your repository
1. Save the image in the `images/` directory
2. Use a descriptive name (e.g., `lipreading-project.jpg`, `chatbot-demo.png`)

### Step 3: Update the HTML
1. Open `index.html`
2. Find the project you want to update
3. Change the image source in the `<img>` tag:
   ```html
   <img src='images/your-project-image.jpg' width=100%>
   ```

### Image tips:
- Use consistent dimensions for a professional look
- Optimize images for web (compress to reduce file size)
- Consider using animated GIFs or MP4s for dynamic demos
- For videos, use this format:
  ```html
  <video width="100%" autoplay loop muted playsinline>
    <source src="images/your-video.mp4" type="video/mp4">
  </video>
  ```

## ➕ How to Add a New Project

To add a new project to your portfolio:

1. Open `index.html`
2. Find the projects table (around line 47, inside `<tbody>` tags)
3. Copy an existing project block (from `<tr>` to `</tr>`)
4. Paste it where you want the new project to appear
5. Update all the details:
   - Image source
   - Project title
   - GitHub link
   - Technology/Language
   - Year
   - Description

Example new project:
```html
<tr>
  <td style="padding:16px;width:20%;vertical-align:middle">
    <img src='images/new-project.jpg' width=100%>
  </td>
  <td style="padding:8px;width:80%;vertical-align:middle">
    <a href="https://github.com/kocsis-david/new-project">
      <span class="papertitle">New Project Name</span>
    </a>
    <br>
    <em>Python</em>, 2025
    <br>
    <a href="https://github.com/kocsis-david/new-project">GitHub</a>
    <p></p>
    <p>
      Description of your new project and what it does.
    </p>
  </td>
</tr>
```

## 📄 How to Add Papers/Publications

If you have academic papers or publications to showcase, you can add a new section between the profile and projects sections.

### Step 1: Add a publications heading
After the profile table (around line 36), add:

```html
<table style="width:100%;border:0px;border-spacing:0px;border-collapse:separate;margin-right:auto;margin-left:auto;"><tbody>
  <tr>
    <td style="padding:16px;width:100%;vertical-align:middle">
      <h2>Publications</h2>
      <p>
        Selected publications and research papers.
      </p>
    </td>
  </tr>
</tbody></table>
```

### Step 2: Add publication entries
After the publications heading, add a table for your papers:

```html
<table style="width:100%;border:0px;border-spacing:0px 10px;border-collapse:separate;margin-right:auto;margin-left:auto;"><tbody>

  <tr>
    <td style="padding:16px;width:20%;vertical-align:middle">
      <img src='images/paper-thumbnail.jpg' width=100%>
    </td>
    <td style="padding:8px;width:80%;vertical-align:middle">
      <a href="PAPER_LINK">
        <span class="papertitle">Paper Title</span>
      </a>
      <br>
      <strong>Author Name</strong>,
      Co-Author Name
      <br>
      <em>Conference/Journal Name</em>, Year
      <br>
      <a href="PAPER_PDF_LINK">PDF</a>
      /
      <a href="ARXIV_LINK">arXiv</a>
      /
      <a href="CODE_LINK">Code</a>
      <p></p>
      <p>
        Brief description or abstract of the paper.
      </p>
    </td>
  </tr>

  <!-- Add more papers here -->

</tbody></table>
```

### Publication tips:
- Add your name in `<strong>` tags to make it stand out
- Include links to: PDF, arXiv, code repository, project page, etc.
- Use paper thumbnails or figures as images
- Order publications by date (newest first) or importance

## 📁 File Structure

```
kocsis-david.github.io/
├── index.html          # Main portfolio page
├── stylesheet.css      # Styling for the website
├── README.md          # This file
├── CNAME              # Custom domain configuration
└── images/            # All images and media
    ├── favicon/       # Favicon files for the site icon
    └── JonBarron.jpg  # Profile photo and project images
```

## 🚀 Deployment

This site is automatically deployed via GitHub Pages:

1. Push your changes to the `main` branch
2. GitHub Pages will automatically rebuild and deploy
3. Your site will be live at `https://kocsis-david.github.io`

### Custom Domain (Optional)
If you want to use a custom domain:
1. Update the `CNAME` file with your domain name
2. Configure your domain's DNS settings to point to GitHub Pages
3. See [GitHub Pages documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site) for details

## 🎨 Customization Tips

### Change colors
Edit `stylesheet.css` to customize the color scheme:
- Link colors: Search for color codes (e.g., `#1772d0`)
- Background: Modify the `body` styles
- Hover effects: Update `.papertitle:hover` and similar classes

### Modify layout
- Adjust table widths to change the image-to-text ratio
- Modify padding values for spacing
- Change font sizes in the CSS

### Add new sections
Follow the same table structure used for projects:
- Create a heading table
- Create a content table with entries
- Style consistently with existing sections

## 🤝 Contributing

This is a personal portfolio site, but feel free to:
- Report issues
- Suggest improvements
- Fork and adapt for your own use

## 📝 License

Website template based on [Jon Barron's design](https://github.com/jonbarron/jonbarron_website).

---

**Last Updated:** November 2025