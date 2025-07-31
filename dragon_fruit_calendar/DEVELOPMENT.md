# Dragon Fruit Calendar - Development Guide

## Project Structure

```
dragon_fruit_calendar/
├── index.html          # Main application file
├── README.md          # Project documentation
├── package.json       # Project configuration and scripts
├── .gitignore        # Git ignore rules
└── DEVELOPMENT.md    # This file
```

## Local Development

### Option 1: Python HTTP Server (Recommended)
```bash
cd dragon_fruit_calendar
python -m http.server 8000 --bind 0.0.0.0
```

### Option 2: Node.js HTTP Server
```bash
cd dragon_fruit_calendar
npm install
npm run serve
```

### Option 3: Using npm scripts
```bash
npm start    # Starts on port 8000
npm run dev  # Starts on port 8080
```

## Accessing via Tailscale

Once the server is running with `--bind 0.0.0.0`, you can access it from any device on your Tailscale network:

- Local: `http://localhost:8000`
- Tailscale: `http://[your-tailscale-ip]:8000`
- LAN: `http://[your-local-ip]:8000`

## Features

- 📅 Visual calendar with pollination tracking
- 📝 Detailed logging (date, time, weather, techniques)
- 📸 Photo uploads with compression
- 🔗 Shareable links
- 💾 Local storage with cleanup tools
- 📱 Mobile-responsive design
- 🔔 Browser notifications for reminders

## Technical Details

- **Frontend**: Pure HTML5, CSS3, JavaScript (no frameworks)
- **Storage**: Browser localStorage with quota management
- **Photos**: Base64 encoding with automatic compression
- **Sharing**: URL-based data encoding for cross-device sync
- **Hosting**: GitHub Pages compatible

## Browser Support

- Chrome/Edge 88+
- Firefox 85+
- Safari 14+
- Mobile browsers with localStorage support

## Storage Limits

- Browser localStorage: ~5-10MB per domain
- Photos are automatically compressed to fit within limits
- Cleanup tools available when storage is full