# Amazon Quick View Extended

A clean, rebuilt Chrome extension for quick viewing Amazon product details without leaving the search results page.

## Features

- **Quick View Buttons**: Click the eye icon (👁️ Quick View) on any Amazon product to see details instantly
- **Product Information**: View price, ratings, reviews, availability, Best Seller Rank (BSR), and key features
- **Smart Caching**: Reduces API calls with 1-minute cache for better performance
- **Customizable Settings**: Control what information to show/hide
- **Product Filters**: Filter by price range, review count, and ratings
- **Clean UI**: Modern, responsive design that works on desktop and mobile

## Installation

1. Download all the files and create this folder structure:
```
amazon-quick-view/
├── manifest.json
├── popup.html
├── js/
│   ├── background.js
│   └── content.js
├── css/
│   └── style.css
└── icons/
    ├── icon16.png
    ├── icon32.png
    ├── icon48.png
    └── icon128.png
```

2. Create icon files (or use placeholder icons):
   - 16x16, 32x32, 48x48, and 128x128 pixel PNG files
   - Name them as shown above and place in the `icons/` folder

3. Load the extension in Chrome:
   - Open Chrome and go to `chrome://extensions/`
   - Enable "Developer mode" in the top right
   - Click "Load unpacked" and select your extension folder

## Usage

### Basic Usage
1. Go to any Amazon website (amazon.com, amazon.co.uk, etc.)
2. Search for products or browse categories
3. Look for the orange "👁️ Quick View" buttons on product listings
4. Click any button to see product details in a popup

### Settings
- Click the extension icon in Chrome's toolbar to access settings
- Toggle the extension on/off
- Customize display options
- Set up product filters
- Hide certain types of products (Prime, sponsored, etc.)

### Quick View Panel
The quick view panel shows:
- **Product title** with Prime badge (if applicable)
- **Price** and availability
- **Customer ratings** and review count
- **Best Seller Rank** (BSR) when available
- **Key product features**
- **Product images**
- **Seller information**

## Key Improvements

This rebuilt version includes:
- ✅ **No external license checks** - works completely offline
- ✅ **Simplified codebase** - easier to maintain and modify
- ✅ **Modern Chrome Extension Manifest V3** compliance
- ✅ **Clean UI/UX** - responsive design that works on all devices
- ✅ **Better error handling** - graceful fallbacks when data isn't available
- ✅ **Performance optimized** - smart caching and efficient DOM manipulation
- ✅ **Privacy focused** - no external API calls or tracking

## Supported Amazon Domains

Works on all major Amazon domains:
- amazon.com (US)
- amazon.co.uk (UK)
- amazon.de (Germany)
- amazon.fr (France)
- amazon.it (Italy)
- amazon.es (Spain)
- amazon.ca (Canada)
- amazon.com.au (Australia)
- amazon.co.jp (Japan)
- And many more...

## Technical Details

- **Manifest Version**: 3 (latest Chrome extension standard)
- **Permissions**: Storage, ActiveTab, Host permissions for Amazon domains
- **Architecture**: Service Worker background script + Content script injection
- **Caching**: 1-minute intelligent cache to reduce network requests
- **Compatibility**: Chrome 88+ (Manifest V3 requirement)

## Customization

You can easily customize the extension by:
- Modifying colors and styles in `css/style.css`
- Adding new product data extraction in `js/content.js`
- Extending filter options in `popup.html`
- Adding new Amazon domains to the manifest

## Troubleshooting

**Quick View buttons not appearing?**
- Make sure the extension is enabled (check the icon in Chrome toolbar)
- Try refreshing the Amazon page
- Check if you're on a supported Amazon domain

**Product data not loading?**
- Check your internet connection
- Some product pages may have different layouts that aren't parsed yet
- Try clearing the extension's cache by reloading the extension

**Settings not saving?**
- Make sure you click "Save Settings" after making changes
- Check Chrome's extension permissions

## Development

To modify or extend the extension:
1. Make changes to the relevant files
2. Go to `chrome://extensions/`
3. Click the refresh icon on your extension
4. Test your changes on Amazon

## License

This is a rebuilt, open-source version. Feel free to modify and distribute as needed.

## Support

If you encounter issues:
1. Check the console for error messages (`F12` → Console tab)
2. Try disabling and re-enabling the extension
3. Reload the Amazon page
4. Make sure you're using a supported Amazon domain