# Portfolio Website - Implementation Guide

## 🎯 Overview
This is your upgraded portfolio website with a modern, professional 4-page structure:

1. **Home (index.html)** - Landing page with hero section, skills, and preview cards
2. **About (about.html)** - Professional background and personal glimpse
3. **Projects & Experience (projects.html)** - Portfolio with expandable project cards and resume
4. **Contact** - Handled via navbar dropdown and global footer

## 📁 Files Included

- `index.html` - Home/Landing page
- `about.html` - About Me page
- `projects.html` - Projects & Experience page
- `styles.css` - Main stylesheet (replaces your old Cover.css and StyleSheet1.css)
- `README.md` - This file

## 🚀 Quick Start

### Step 1: Prepare Your Files
1. Download all HTML and CSS files
2. Keep your existing `ProHeadshot.jpg` image in the same folder
3. (Optional) Add your resume PDF to the folder

### Step 2: Update Image References
If your headshot has a different filename, update line 59 in `index.html`:
```html
<img src="YOUR-IMAGE-NAME.jpg" alt="Parker Hewett Professional Headshot" class="hero-image">
```

### Step 3: Add Resume (Optional)
1. Place your resume PDF in the same folder (e.g., `Parker_Hewett_Resume.pdf`)
2. In `projects.html`, find the resume section (around line 409)
3. Uncomment the iframe code and update the src:
```html
<iframe 
    src="Parker_Hewett_Resume.pdf" 
    class="resume-embed"
    title="Parker Hewett Resume">
</iframe>
```
4. Update the download button on line 395:
```html
<a href="Parker_Hewett_Resume.pdf" class="btn btn-primary" download>
    Download Resume (PDF)
</a>
```

### Step 4: Add Personal Photos (Optional)
In `about.html` (line 175), you can add personal photos:
1. Uncomment the photo grid code
2. Replace placeholder filenames with your actual image files:
```html
<div class="photo-grid">
    <img src="photo1.jpg" alt="Photography work">
    <img src="photo2.jpg" alt="Leadership activities">
    <img src="photo3.jpg" alt="Personal projects">
    <img src="photo4.jpg" alt="Community involvement">
</div>
```

## 📤 Deployment to GitHub Pages

### Method 1: Replace Existing Files
1. In Visual Studio, delete your old HTML and CSS files
2. Add these new files to your repository
3. Commit and push:
```bash
git add .
git commit -m "Portfolio website upgrade - modern 4-page structure"
git push origin main
```

### Method 2: New Repository
1. Create a new repository named `yourusername.github.io`
2. Add all files to the repository
3. Push to GitHub
4. Go to Settings > Pages
5. Select your main branch
6. Your site will be live at `https://yourusername.github.io`

## ✨ Key Features

### ✅ Responsive Design
- Mobile-first approach
- Sticky header on desktop
- Hamburger menu on mobile
- All sections adapt to screen size

### ✅ Modern Navigation
- Contact dropdown with external link indicators
- Smooth transitions and hover effects
- Mobile overlay navigation

### ✅ Interactive Elements
- Expandable project cards with detailed information
- Filter buttons for projects (All, Data Systems, Reporting, etc.)
- Smooth animations and transitions

### ✅ Professional Footer
- Global footer on all pages
- Email, LinkedIn, and GitHub links
- Clean, consistent design

## 🎨 Customization Guide

### Colors
Update colors in `styles.css` (lines 4-13):
```css
:root {
    --primary-color: #459fbb;      /* Main brand color */
    --primary-dark: #357a91;       /* Darker shade */
    --secondary-color: #63639f;    /* Accent color */
    /* ... etc ... */
}
```

### Skills
Update skills in `index.html` (lines 79-90) and `about.html` (lines 62-71)

### Projects
Add/edit projects in `projects.html` starting at line 78. Each project follows this structure:
```html
<div class="project-card" data-category="data-systems automation">
    <div class="project-header" onclick="toggleExpand(this)">
        <!-- Project title and expand button -->
    </div>
    <p class="project-summary">
        <!-- Brief summary -->
    </p>
    <div class="project-details">
        <!-- Detailed information (hidden until expanded) -->
    </div>
</div>
```

## 📱 Testing Checklist

- [ ] Test on desktop browsers (Chrome, Firefox, Safari)
- [ ] Test on mobile devices
- [ ] Verify all links work (especially email and external links)
- [ ] Check that contact dropdown works
- [ ] Test hamburger menu on mobile
- [ ] Verify project cards expand/collapse
- [ ] Test filter buttons on projects page
- [ ] Check resume embed (if applicable)
- [ ] Verify all images load correctly

## 🐛 Troubleshooting

### Images Not Loading
- Ensure image files are in the same directory as HTML files
- Check that filenames match exactly (case-sensitive)
- Verify image file extensions (.jpg, .png, etc.)

### Resume Not Displaying
- Some mobile browsers don't render PDFs well in iframes
- The fallback link ensures users can still access it
- Consider using Google Drive embed as alternative

### Styling Issues
- Clear browser cache (Ctrl+Shift+R or Cmd+Shift+R)
- Ensure `styles.css` is in the same directory as HTML files
- Check browser console for errors (F12)

## 📧 Contact Information

Current contact links in the site:
- Personal: pehewett@hotmail.com
- OU Email: parker.hewett@ou.edu
- LinkedIn: linkedin.com/in/parker-hewettou/
- GitHub: github.com/Parkerhewett

## 🔄 Future Enhancements

Consider adding:
- [ ] Blog section for technical articles
- [ ] Photo gallery for photography work
- [ ] Dark mode toggle
- [ ] Google Analytics
- [ ] Contact form (requires backend)
- [ ] PDF resume auto-download on button click
- [ ] Testimonials section
- [ ] Skills proficiency bars/charts

## 📝 Notes

- All external links open in new tabs (target="_blank")
- Site is fully accessible with semantic HTML
- SEO-friendly with proper meta tags and alt text
- Fast loading with minimal dependencies (no heavy frameworks)
- Works without JavaScript (progressive enhancement)

---

**Version:** 1.0  
**Last Updated:** January 2025  
**Built for:** Parker Hewett  
