# 📖 Tom Riddle's Diary

An immersive, interactive web experience that brings Tom Riddle's diary from Harry Potter to life. Write in the diary and watch as it writes back with Tom's charming yet subtly menacing personality.

![Diary Preview](https://img.shields.io/badge/Magic-Dark%20Arts-purple?style=for-the-badge)

## ✨ Features

### Visual Design
- **Dark Leather Cover** - Vintage leather-bound aesthetic with realistic texture
- **Aged Parchment** - Authentic parchment paper with subtle aging effects
- **Gothic Typography** - Cinzel and Cormorant Garamond fonts for that magical feel
- **3D Book Layout** - Realistic open book with spine and page shadows

### Interactions
- **Ink Writing Animation** - Text appears as if written by an invisible quill
- **Tom's Responses** - AI-like responses in Tom Riddle's distinctive voice
- **Page Turn Animations** - Smooth 3D page turning effects
- **LocalStorage Memory** - The diary remembers your conversations

### Special Effects
- 🪄 **Magical Particles** - Floating dust and sparkles that follow your cursor
- 🩸 **Ink Bleed Effect** - Text bleeds into the page when Tom writes
- ✨ **Magical Glow** - Subtle green glow around Tom's messages
- 🎵 **Sound Visualization** - Visual feedback for writing sounds
- 🩸 **Blood Drip** - Secret Easter egg reveals dark surprises
- 🔮 **The Diary Learns** - It remembers your secrets and references them later

### Easter Eggs
- Type "Tom Marvolo Riddle" or "I am Lord Voldemort" for a surprise...
- Use the Konami code (↑↑↓↓←→←→BA) for a dark revelation
- Write enough messages and the diary reveals it knows your secrets

## 🚀 How to Run

### Option 1: Open Directly
Simply open `index.html` in any modern web browser:
```bash
# On macOS
open index.html

# On Linux
xdg-open index.html

# On Windows
start index.html
```

### Option 2: Local Server (Recommended)
For the best experience with all features working properly:

```bash
# Using Python 3
python -m http.server 8080

# Using Python 2
python -m SimpleHTTPServer 8080

# Using Node.js (npx)
npx serve

# Using PHP
php -S localhost:8080
```

Then open http://localhost:8080 in your browser.

## 📁 File Structure

```
tom-riddle-diary/
├── index.html          # Complete diary application (all-in-one)
└── README.md          # This file
```

**Note:** This is a single-file application! All CSS, JavaScript, and assets are embedded for easy deployment.

## 🎮 How to Use

1. **Open the diary** - Click "Open the Diary" on the warning screen
2. **Write your thoughts** - Type in the input field at the bottom right
3. **Press Enter** - Watch as Tom writes back with his elegant, cursive responses
4. **Keep writing** - The more you share, the more the diary learns...

## 🔧 Browser Compatibility

- ✅ Chrome/Edge (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Mobile browsers (responsive design)

## 🎨 Customization

### Changing the Color Scheme
Edit the CSS variables in the `:root` selector:
```css
:root {
    --leather-dark: #1a0f0f;    /* Diary cover */
    --parchment: #f4e8d0;        /* Page color */
    --ink-dark: #0d0d0d;         /* User text */
    --ink-blood: #3d1a1a;        /* Tom's text */
    --glow-green: #2d5016;       /* Magical glow */
}
```

### Adding More Responses
Find the `tomResponses` object in the JavaScript and add to any category:
```javascript
const tomResponses = {
    greetings: [
        "Your custom greeting here...",
        // ... more responses
    ],
    // ... other categories
};
```

## ⚠️ Warning

This diary once belonged to Tom Marvolo Riddle. Those who write in it may find that it writes back... and remembers.

---

*"I can show you things. I can make things happen. All I need is for you to tell me your secrets..."*

🍺 Built with dark magic and a touch of lobster energy