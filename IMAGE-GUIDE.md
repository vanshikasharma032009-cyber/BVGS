# 📸 Image Guide for Bal Vikas Global School Website

This guide explains how images work in the website and how to add new ones.

## 📁 Current Image Structure

### Root `images/` Folder:
| File | Used In | Type |
|------|---------|------|
| `hero-building.svg` | Homepage hero background | SVG |
| `school-building.jpg` | Homepage hero featured image | JFIF |
| `logo.svg` | Header, footer, all pages | SVG |
| `about-building.svg` | About section background | SVG |
| `gallery-1.svg` to `gallery-8.svg` | Gallery page | SVG (8 images) |
| `download.jfif` / `download (1).jfif` | General use | JFIF |

### `bal vikas/` Subfolder:
| File | Description |
|------|-------------|
| `building.svg` | School building icon |
| `classroom.svg` | Classroom icon |
| `school-icon.svg` | School representative icon |

---

## ✅ How to Add New Images

### **Step 1: Place the image file**
Put your new image in one of these locations:
- `/workspaces/my-project/images/` (recommended for website images)
- `/workspaces/my-project/images/bal vikas/` (for icon-style images)

**Supported formats:**
- `.svg` - Best for logos, icons, scalable graphics
- `.jpg` / `.jpeg` - Best for photographs
- `.png` - Good for graphics with transparency

### **Step 2: Reference in HTML**
Use relative paths from the HTML file location (`index.html` is at project root):

```html
<!-- For images in the root images/ folder -->
<img src="images/your-image.jpg" alt="Description">

<!-- For images in subfolders -->
<img src="images/bal vikas/your-icon.svg" alt="Description">
```

### **Step 3: Add CSS if needed**
If you want to style the new image, add rules to `/workspaces/my-project/css/style.css`.

### **Step 4: Update HTML navigation (if needed)**
If adding to the gallery or features section, update the corresponding HTML file.

---

## 🖼️ Adding to Specific Sections

### **Hero Section (`index.html`):**
```html
<!-- Replace existing hero image -->
<img src="images/your-new-hero.jpg" alt="Bal Vikas Global School Campus">
```

### **Gallery Section (`gallery.html`):**
```html
<!-- Add new gallery item -->
<div class="gallery-item" data-category="your-category">
  <img src="images/your-gallery.jpg" alt="Description">
  <div class="gallery-overlay">...</div>
  <div class="gallery-info">
    <h4>Your Title</h4>
    <p>Your caption</p>
  </div>
</div>
```

### **About Section (`about.html`):**
```html
<!-- Replace about building image -->
<img src="images/your-about.jpg" alt="Bal Vikas Global School Campus">
```

### **Footer/Navbar (`index.html`, `about.html`, etc.):**
```html
<!-- Logo replacement -->
<img src="images/your-logo.svg" alt="Bal Vikas Global School Logo">
```

---

## 🔧 Image Best Practices

### **File Naming:**
- Use lowercase letters, numbers, hyphens
- Avoid spaces: `school-building.jpg` ✅, `School Building.jpg` ❌
- Example: `admission-form.jpg`, `facility-lab.jpg`, `student-art.jpg`

### **Optimization:**
- **SVG**: No optimization needed - vectors scale perfectly
- **JPG/PNG**: Compress before uploading (keep under 200KB for web)
- Use appropriate dimensions:
  - Hero images: 1200px wide max
  - Gallery images: 300-400px wide
  - Logos: 50-100px high

### **Accessibility:**
Always include `alt` text:
```html
<img src="images/image.jpg" alt="Descriptive alt text">
```
Example: `alt="Bal Vikas Global School campus building"` or `alt="School laboratory with modern equipment"`

---

## 🚫 Common Issues & Fixes

### **1. Image not showing**
- ✅ Check the file path is correct
- ✅ Verify the file exists in the right folder
- ✅ Ensure the filename matches exactly (case-sensitive on Linux)
- ✅ Check HTML `<img>` tag for typos

### **2. Broken image icon**
- ✅ File path wrong - correct the `src` attribute
- ✅ File not uploaded - upload the image first
- ✅ Wrong file format - use supported formats (.jpg, .png, .svg)

### **3. Image too large/small**
- ✅ CSS controls size: `width: 100%; height: auto;`
- ✅ Add `style="max-width: 500px;"` directly in `<img>` tag
- ✅ Modify CSS `.facility-image`, `.gallery-item`, etc.

### **4. Wrong image on wrong page**
- ✅ Each HTML file references its own images
- ✅ Don't share `hero-building.svg` on the about page unless intended
- ✅ Copy or reference appropriately

---

## 📸 Example: Adding a New Facilities Image

**Step 1:** Place `library.jpg` in `/workspaces/my-project/images/`

**Step 2:** Add to `facilities.html`:
```html
<div class="facility-card">
  <div class="facility-image" style="background: none;">
    <img src="images/library.jpg" alt="School library with books and study tables">
  </div>
  <div class="facility-content">
    <h3>Library</h3>
    <p>Well-stocked library with digital resources</p>
  </div>
</div>
```

**Step 3:** The CSS will automatically style it (the `.facility-image` class sets background and font-size, but the img will overlay)

---

## 💡 Quick Commands

**List all images:**
```bash
ls -la /workspaces/my-project/images/
```

**Count images:**
```bash
ls /workspaces/my-project/images/*.jpg | wc -l
ls /workspaces/my-project/images/*.svg | wc -l
```

**Check image sizes:**
```bash
ls -la /workspaces/my-project/images/ | grep -E "\.(jpg|jpeg|png|svg)$"
```

---

**Need help with a specific image addition?** Tell me:
- What type of image (photo, icon, illustration)?
- Where you want to use it (hero, gallery, about, facilities)?
- What should it show/describe?

And I'll give you the exact code to add it! ✅