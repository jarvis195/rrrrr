# Resource Library

Interactive learning materials hosted via GitHub Pages.

## Setup

1. Enable GitHub Pages in repo settings (Settings > Pages > Source: Deploy from branch > main)
2. Access at `https://[username].github.io/rrrrr/`

## Adding Content

1. Open `encoder.html` in browser (or via Pages URL)
2. Paste your HTML content
3. Click "Encode"
4. Save output as `games/[name].dat`
5. Add entry to `index.html` games array:

```javascript
{
    id: 'yourname',           // matches filename without .dat
    title: 'Display Title',
    description: 'Short description'
}
```

## Structure

```
/
├── index.html      # Main page with game list
├── play.html       # Decoder/player
├── encoder.html    # Encoding tool
└── games/
    └── *.dat       # Encoded content files
```

## How It Works

Content is encoded with ROT13 + Base64. The player decodes and renders in an iframe.
