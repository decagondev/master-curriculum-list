# Sprint Folder Styling Guide

## Overview
This guide provides instructions for consistently styling sprint folders containing educational content. Each sprint folder typically contains multiple objective files that need to be styled with a modern, responsive design.

## File Structure
Each sprint folder follows this general structure:
```
Sprint_Folder/
├── objective-01-*.html
├── objective-02-*.html
├── objective-03-*.html
...
├── welcome.html
├── tech-requirements.html
└── unit-overview.html
```

## Required Styling Elements

### 1. Common Elements for All Files
- Responsive layout with max-width: 1200px
- Modern font stack (Arial, sans-serif)
- Consistent color scheme:
  - Primary: #93005a
  - Secondary: #00808c
  - Background: #f5f5f5
  - Text: #333
  - Links: #333 (normal), white (hover)

### 2. Navigation
- Back to Sprint Content link
- Unit Videos link
- Hover effects with color transition

### 3. Content Structure
- Clear section headings
- Content sections with white background and subtle shadow
- Proper spacing and margins
- Responsive video containers (16:9 ratio)

### 4. Interactive Elements
- Tab system for video content
- Hover effects on interactive elements
- Smooth transitions

### 5. Video Integration
- Wistia video embeds
- Responsive containers
- Proper iframe attributes

## Implementation Steps

1. **Base Styling**
   ```css
   body {
       font-family: Arial, sans-serif;
       max-width: 1200px;
       margin: 0 auto;
       padding: 20px;
       background-color: #f5f5f5;
       line-height: 1.6;
       color: #333;
   }
   ```

2. **Navigation**
   ```css
   .nav {
       display: flex;
       gap: 20px;
       margin-bottom: 30px;
   }
   .nav a {
       text-decoration: none;
       color: #333;
       padding: 10px 20px;
       border-radius: 5px;
       background-color: #fff;
       transition: background-color 0.3s;
   }
   ```

3. **Content Sections**
   ```css
   .content-section {
       background: white;
       padding: 30px;
       margin-bottom: 30px;
       border-radius: 10px;
       box-shadow: 0 2px 5px rgba(0,0,0,0.1);
   }
   ```

4. **Video Containers**
   ```css
   .video-container {
       position: relative;
       padding-bottom: 56.25%;
       height: 0;
       overflow: hidden;
       max-width: 100%;
       margin: 20px 0;
   }
   ```

5. **Tab System**
   ```css
   .tabs {
       margin: 20px 0;
   }
   .tab-list {
       display: flex;
       gap: 10px;
       border-bottom: 2px solid #dee2e6;
   }
   ```

## JavaScript Requirements

1. **Tab Functionality**
```javascript
function openTab(evt, tabName) {
    var i, tabcontent, tabbuttons;
    
    tabcontent = document.getElementsByClassName("tab-content");
    for (i = 0; i < tabcontent.length; i++) {
        tabcontent[i].style.display = "none";
    }
    
    tabbuttons = document.getElementsByClassName("tab-button");
    for (i = 0; i < tabbuttons.length; i++) {
        tabbuttons[i].className = tabbuttons[i].className.replace(" active", "");
    }
    
    document.getElementById(tabName).style.display = "block";
    evt.currentTarget.className += " active";
}
```

## HTML Template Structure
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>[Objective Title]</title>
    <style>
        /* Insert common styles here */
    </style>
</head>
<body>
    <div class="nav">
        <a href="../[sprint]-content.html">← Back to Sprint Content</a>
        <a href="../[unit]-videos.html">Unit Videos</a>
    </div>

    <h1 class="section-title">[Page Title]</h1>
    
    <div class="content-section">
        <div class="objective-content">
            <!-- Content goes here -->
        </div>
    </div>
</body>
</html>
```

## Quality Checklist
- [ ] Responsive design works on all screen sizes
- [ ] All videos are properly embedded
- [ ] Navigation links are working
- [ ] Tabs function correctly
- [ ] Styles are consistent across all pages
- [ ] No CSS conflicts
- [ ] JavaScript functions are properly scoped
- [ ] All interactive elements have hover states
- [ ] Content is properly formatted and readable
- [ ] Videos are responsive and maintain aspect ratio

## Notes
- Maintain consistency across all sprint folders
- Test on multiple browsers and devices
- Ensure accessibility standards are met
- Keep styles modular and reusable
- Document any custom modifications needed for specific sprints 