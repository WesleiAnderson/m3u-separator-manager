# 📺 M3U Separator Manager

Web application to parse and organize M3U/M3U8 playlists by category with automatic ZIP export. Includes HTML UI, file upload, and category separation for IPTV lists.

## 🎯 Features

- **📥 Direct Link Download**: Download M3U files directly from URLs (supports HTTP/HTTPS with optional S forcing)
- **📁 File Upload**: Upload your own M3U/M3U8 playlist files
- **🏷️ Automatic Category Separation**: Automatically parses `group-title` metadata and organizes channels by category
- **📦 ZIP Export**: Downloads all categorized playlists as a single ZIP file
- **🎨 User-Friendly Interface**: Clean, intuitive UI with progress tracking
- **⚡ Client-Side Processing**: All processing happens in the browser - no server needed!
- **✨ Optional Suffixes**: Add custom suffixes to categorized files (e.g., "⭐ Premium", "🧃 Kids")

## 🚀 Usage

1. **Option A: From URL**
   - Paste your M3U list URL in the "Link da lista .M3U" field
   - Click "🔓 BAIXAR ARQUIVO M3U BRUTO" to download the raw file
   - Follow steps below to process it

2. **Option B: From Local File**
   - Click "📁 AGORA BOTE AQUI esse arquivo .M3U"
   - Select your M3U/M3U8 file from your computer
   - (Optional) Add a suffix in "✍️ Complemento opcional"
   - Click "⚙️ Processar Arquivo M3U e BAIXAR!"

3. **Result**
   - A ZIP file will download containing separate M3U files for each category
   - Files are named based on category (e.g., `Filmes.m3u`, `Esportes.m3u`)

## 📋 M3U File Format

The app expects M3U files with the following format:

```
#EXTM3U
#EXTINF:-1 group-title="Category Name",Channel Name
http://stream-url.com/stream
#EXTINF:-1 group-title="Category Name",Another Channel
http://another-stream.com/stream
```

## 💻 Technical Details

- **Frontend**: HTML5 + JavaScript (Vanilla JS)
- **Libraries**: 
  - [JSZIP](https://cdnjs.cloudflare.com/ajax/libs/jszip/3.10.0/jszip.min.js) - ZIP file creation
- **Processing**: FileReader API, RegExp parsing
- **Browser Compatibility**: All modern browsers (Chrome, Firefox, Safari, Edge)

## 🔒 Privacy

This application is completely client-side. No data is sent to any server:
- Files are processed locally in your browser
- No uploads to external services
- No tracking or analytics
- Safe for personal and private use

## 📦 Installation

Simply open `index.html` in your web browser. No installation required!

### Local Server (Optional)
For development or advanced usage:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js
npx http-server

# Using PHP
php -S localhost:8000
```

Then visit `http://localhost:8000`

## 🛠️ Development

### File Structure
```
m3u-separator-manager/
├── index.html          # Main application
├── README.md           # This file
└── .gitignore          # Git ignore rules
```

### Future Enhancements
- Support for M3U extended info parsing
- Playlist validation and error checking
- Drag & drop file upload
- Custom category filtering
- Support for M3U8 encryption/DRM handling
- Backend API integration

## 📝 License

MIT License - Free to use and modify

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report issues
- Suggest features
- Submit pull requests
- Improve documentation

## 📮 Support

For issues, questions, or suggestions, please open an [issue](https://github.com/WesleiAnderson/m3u-separator-manager/issues).

---

**Made with ❤️ for IPTV enthusiasts**
