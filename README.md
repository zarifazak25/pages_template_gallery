# Template Gallery - Setup Instructions

## Quick Start

1. **Rename the file** to `index.html`
2. **Choose your screenshot method** (see below)
3. **Add your template URLs** to the templates array
4. **Upload to your GitHub Pages repository**

## Screenshot Options

The gallery can automatically generate preview images from your live websites! Choose one of these methods:

### Option 1: ScreenshotOne (Recommended - Free)
**Best for: Beginners, free tier available**

1. Change line 7 to: `const SCREENSHOT_SERVICE = 'screenshotone';`
2. Just add your template URLs - screenshots generate automatically!
3. Free tier: 100 screenshots/month
4. Optional: Sign up at [screenshotone.com](https://screenshotone.com) for higher limits

### Option 2: Microlink (Free Alternative)
**Best for: Backup option**

1. Change line 7 to: `const SCREENSHOT_SERVICE = 'microlink';`
2. Free tier available
3. Visit [microlink.io](https://microlink.io) for details

### Option 3: Manual Screenshots
**Best for: Complete control over images**

1. Change line 7 to: `const SCREENSHOT_SERVICE = 'manual';`
2. Take your own screenshots
3. Add `customImage: "path/to/screenshot.png"` to each template
4. Store images in your repo's `images/` folder

## How to Add Your Templates

Find this section in the HTML file (around line 143):

```javascript
const templates = [
    {
        title: "Modern Portfolio",
        previewUrl: "https://yourusername.github.io/modern-portfolio/",
        repoUrl: "https://github.com/yourusername/modern-portfolio",
        pageType: "one-page",
        techStack: "html-css-js",
        customImage: "" // Optional: only needed if using manual screenshots
    },
    // Add more templates here...
];
```

### For Each Template:

- **title**: The name of your template
- **previewUrl**: The live GitHub Pages URL (screenshots auto-generate from this!)
- **repoUrl**: The GitHub repository URL
- **pageType**: Either `"one-page"` or `"multi-page"`
- **techStack**: Either `"html-css"` or `"html-css-js"`
- **customImage**: (Optional) Override with your own screenshot path

## Example: Adding Your Real Templates

```javascript
const templates = [
    {
        title: "Portfolio Site",
        previewUrl: "https://yourname.github.io/portfolio/",
        repoUrl: "https://github.com/yourname/portfolio",
        pageType: "one-page",
        techStack: "html-css-js"
    },
    {
        title: "Business Page",
        previewUrl: "https://yourname.github.io/business-template/",
        repoUrl: "https://github.com/yourname/business-template",
        pageType: "multi-page",
        techStack: "html-css"
    }
];
```

That's it! The screenshots will be generated automatically from your live sites.

## Customization

### Change Colors
Edit the CSS gradient background (line 21):
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Adjust Card Size
Edit the grid template (line 79):
```css
grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
```

## Publishing to GitHub Pages

1. Create a new repository (or use existing)
2. Upload the file as `index.html`
3. Go to Settings > Pages
4. Select your branch and save
5. Your gallery will be live at `https://yourusername.github.io/repo-name/`

## Tips

- Screenshots update automatically when you reload the page
- Make sure your template sites are live before adding them
- The first load might be slower as screenshots generate
- Screenshots are cached by the service for faster subsequent loads

## Troubleshooting

**Screenshots not showing?**
- Check that your template URLs are live and accessible
- Try a different screenshot service
- Switch to manual screenshots as a fallback

**Want better quality screenshots?**
- Use manual screenshots with higher resolution
- Take screenshots at 1920x1200 and save to `images/` folder
