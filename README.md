# SecurePass Pro - Password Generator

<div align="center">

![SecurePass Pro Logo](https://img.shields.io/badge/SecurePass-Pro-667eea?style=for-the-badge&logo=security&logoColor=white)

**Customizable password generator with modern design**

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Responsive](https://img.shields.io/badge/Responsive-Design-00C4CC?style=flat-square)](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design)

**[🚀 Live Demo - Click Here to Use](https://aman-bam.github.io/Professional-Password-Generator/)**

[Features](#features) • [Installation](#installation) • [Customization](#customization) • [Usage](#usage)

</div>

## 🔐 Overview

<img width="1918" height="970" alt="Screenshot 2025-07-28 132156" src="https://github.com/user-attachments/assets/d0103178-592f-4fb1-8ca6-74a28c1445c9" />


SecurePass Pro is a client-side password generator built with pure HTML, CSS, and JavaScript. It features a modern, responsive design with comprehensive customization options, making it perfect for white-labeling or integration into existing projects.

## ✨ Features

### 🎯 Core Functionality
- **Password Generation**: 4-50 character passwords with multiple character sets
- **Real-time Strength Analysis**: 10-point scoring system with detailed feedback
- **Preset Templates**: Basic (8), Standard (12), Secure (16), Maximum (24) character presets
- **Character Options**: Uppercase, lowercase, numbers, special characters
- **Similar Character Exclusion**: Optional removal of confusing characters (0, O, l, 1, I)
- **Password History**: In-memory storage of last 10 generated passwords

### 🎨 User Interface
- **Modern Design**: Glassmorphism effects with gradient backgrounds
- **Responsive Layout**: Works on desktop, tablet, and mobile devices
- **Smooth Animations**: Hover effects, transitions, and micro-interactions
- **Accessibility**: Proper contrast ratios and semantic HTML
- **Dark Theme**: Purple gradient color scheme

### ⚡ Advanced Features
- **Bulk Generation**: Create 5 or 10 passwords at once
- **Export Functionality**: Download password history as text file
- **Copy to Clipboard**: One-click copying with visual feedback
- **Keyboard Shortcuts**: Quick actions for power users
- **Auto-regeneration**: Passwords update when settings change

### 🏢 Customization
- **Brand Configuration**: Easy logo, title, and company customization
- **Color Themes**: Customizable CSS variables for branding
- **White-label Ready**: Complete branding control via CONFIG object

## 🚀 Installation

### Simple Setup
1. **Download the file**:
   ```bash
   # Download index.html to your desired location
   wget https://your-repo/index.html
   ```

2. **Open in browser**:
   ```bash
   # Double-click the file or open with any modern browser
   open index.html      # macOS
   start index.html     # Windows
   xdg-open index.html  # Linux
   ```

### Web Server Hosting
```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve .

# Then visit http://localhost:8000
```

## 🎨 Customization

### Brand Configuration

Modify the CONFIG object at the top of the JavaScript section:

```javascript
const CONFIG = {
    brand: {
        logo: 'SP',                           // Logo initials
        title: 'SecurePass',                  // Main title
        subtitle: 'Professional Password Generator', // Subtitle
        tagline: 'Enterprise-grade security for your business', // Tagline
        company: 'Your Company Name'          // Footer text
    },
    colors: {
        primary: '#667eea',                   // Primary color
        secondary: '#764ba2',                 // Secondary color
        accent: '#4caf50'                     // Success color
    },
    defaults: {
        length: 16,                           // Default length
        uppercase: true,
        lowercase: true,
        numbers: true,
        symbols: true,
        excludeSimilar: false
    }
};
```

### Color Customization

Update CSS custom properties:

```css
:root {
    --primary-color: #667eea;     /* Your brand primary */
    --secondary-color: #764ba2;   /* Your brand secondary */
    --accent-color: #4caf50;      /* Success/accent color */
    --text-color: #333;           /* Text color */
    --bg-light: #f8f9fa;          /* Light background */
    --border-color: #ddd;         /* Border color */
}
```

### Logo Replacement

Replace text logo with image:

```html
<!-- Find this in the HTML -->
<div class="brand-logo" id="brandLogo">SP</div>

<!-- Replace with -->
<div class="brand-logo">
    <img src="logo.png" alt="Logo" style="width: 40px; height: 40px; border-radius: 8px;">
</div>
```

## 📖 Usage

### Basic Usage
1. **Set Length**: Enter desired password length (4-50 characters)
2. **Choose Character Types**: Check/uncheck uppercase, lowercase, numbers, symbols
3. **Select Preset**: Use dropdown for quick configurations
4. **Generate**: Click "Generate Secure Password" or press Ctrl+G
5. **Copy**: Click copy button or press Ctrl+C

### Advanced Features

#### Bulk Generation
- Click "Generate 5" or "Generate 10" for multiple passwords
- All passwords copied to clipboard automatically

#### Password History
- Last 10 passwords stored in "Recent Passwords" section
- Click "Copy" next to any previous password
- "Clear All" removes history

#### Export Passwords
- Click "Export All" to download history as text file
- Useful for saving generated passwords

### Keyboard Shortcuts
| Shortcut | Action |
|----------|--------|
| `Ctrl/Cmd + G` | Generate new password |
| `Ctrl/Cmd + C` | Copy current password |
| `Ctrl/Cmd + R` | Regenerate password |
| `Enter` | Generate (when in length field) |

## 🔒 Security Information

### Password Generation
- Uses JavaScript's `Math.random()` for generation
- Ensures at least one character from each selected type
- Shuffles final password to avoid predictable patterns
- No external dependencies or network requests

### Strength Analysis
The strength meter evaluates passwords on a 10-point scale:

| Criteria | Points | Requirements |
|----------|--------|-------------|
| **Length** | 2-4 | 8+ chars (2pts), 12+ (1pt), 16+ (1pt) |
| **Uppercase** | 1 | Contains A-Z |
| **Lowercase** | 1 | Contains a-z |
| **Numbers** | 1 | Contains 0-9 |
| **Symbols** | 1 | Contains special characters |
| **Entropy** | 2 | High character variety + length ≥12 |

### Privacy & Security
- **Client-side Only**: No data sent to servers
- **No Persistent Storage**: Passwords only stored in memory during session
- **No External Requests**: Self-contained application
- **Browser Storage**: Does not use localStorage or sessionStorage

## 📱 Browser Support

| Browser | Version | Status |
|---------|---------|--------|
| Chrome | 60+ | ✅ Full support |
| Firefox | 55+ | ✅ Full support |
| Safari | 12+ | ✅ Full support |
| Edge | 79+ | ✅ Full support |
| Mobile Safari | 12+ | ✅ Responsive |
| Chrome Mobile | 60+ | ✅ Touch-optimized |

## 🛠️ Technical Details

### File Structure
```
index.html          # Complete application (HTML + CSS + JS)
├── HTML Structure  # Semantic markup
├── CSS Styles     # Modern responsive design
└── JavaScript     # Password generation logic
```

### Key Functions
- `createPass()` - Main password generation
- `updateStrengthMeter()` - Real-time strength analysis
- `copyPass()` - Clipboard functionality
- `generateBulk()` - Multiple password creation
- `applyPreset()` - Quick configuration presets

### Performance
- **File Size**: ~35KB (single HTML file)
- **Load Time**: < 100ms on modern browsers
- **Memory Usage**: < 2MB typical
- **Generation Speed**: Instant (< 5ms)

## 🎯 Use Cases

### Personal Use
- Generate secure passwords for personal accounts
- Learn about password security best practices
- Quick password creation with visual strength feedback

### Development Projects
- Integrate into web applications
- White-label for client projects
- Reference for password generation logic

### Small Business
- Branded password generator for employees
- Customer-facing security tool
- Training tool for password best practices

## 🔧 Customization Examples

### Minimal Branding
```javascript
const CONFIG = {
    brand: {
        logo: 'PG',
        title: 'Password Generator',
        subtitle: 'Secure Password Creation',
        tagline: 'Stay secure online',
        company: 'My Company'
    }
};
```

### Corporate Theme
```css
:root {
    --primary-color: #1e40af;    /* Corporate blue */
    --secondary-color: #1e3a8a;  /* Darker blue */
    --accent-color: #10b981;     /* Success green */
}
```

## 📄 License

This project is available under the MIT License. Feel free to use, modify, and distribute.

## 🤝 Contributing

1. Fork the repository
2. Make your changes to `index.html`
3. Test in multiple browsers
4. Submit a pull request

## 📞 Support

- **Issues**: Report bugs or request features
- **Documentation**: All features documented in this README
- **Updates**: Check for new versions periodically

---

<div align="center">

**SecurePass Pro** - *Simple, Secure, Customizable*

Made with modern web technologies for reliable password generation

[⬆ Back to Top](#securepass-pro---password-generator)

</div>
