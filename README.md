# Check Organic User - WordPress Plugin

A lightweight WordPress plugin that detects organic traffic and displays different navigation menus based on user browser detection.

## 📋 Description

Check Organic User is a WordPress plugin designed to enhance user experience by displaying customized menus for organic traffic. The plugin detects the visitor's browser and sets a cookie to identify them as an organic user, then automatically switches the navigation menu from the default to an "Organic Menu".

## ✨ Features

- **Browser Detection**: Identifies major browsers including:
  - Google Chrome
  - Mozilla Firefox
  - Safari
  - Microsoft Edge
  - Opera & Opera Mini
  - Internet Explorer
- **Automatic Menu Switching**: Seamlessly switches from "Main menu" to "Organic Menu" for organic visitors
- **Cookie-Based Tracking**: Sets a 30-day cookie to remember organic users
- **Lightweight & Fast**: Minimal code footprint with no database queries
- **Theme Location Support**: Works with both menu names and theme locations

## 🚀 Installation

### Method 1: Manual Installation

1. Download the plugin files
2. Upload the `check-organic-user` folder to `/wp-content/plugins/` directory
3. Activate the plugin through the 'Plugins' menu in WordPress
4. Create a menu named "Organic Menu" in Appearance > Menus
5. The plugin will automatically start working

### Method 2: Upload via WordPress Admin

1. Go to Plugins > Add New
2. Click "Upload Plugin"
3. Choose the downloaded zip file
4. Click "Install Now" and then "Activate"

## 🔧 Configuration

1. **Create Your Menus**:
   - Go to `Appearance > Menus`
   - Create two menus:
     - "Main menu" (for regular traffic)
     - "Organic Menu" (for organic traffic)

2. **Assign Theme Location**:
   - Assign "Main menu" to your primary theme location
   - The plugin will automatically switch to "Organic Menu" for organic users

## 📖 How It Works

1. When a user visits your site, the plugin detects their browser from the User-Agent string
2. If a valid browser is detected, a cookie named `organic_user` is set for 30 days
3. On subsequent page loads, the plugin checks for this cookie
4. If the cookie exists, the navigation menu is automatically switched from "Main menu" to "Organic Menu"

## 🎯 Use Cases

- Display different navigation for first-time organic visitors
- A/B testing different menu structures
- Customized user journeys for organic traffic
- SEO-optimized navigation paths
- Landing page optimization

## 🔍 Technical Details

- **Cookie Name**: `organic_user`
- **Cookie Duration**: 30 days
- **Cookie Path**: Site-wide (`/`)
- **Hook Used**: `init` for detection, `wp_nav_menu_args` for menu switching

## ⚙️ Requirements

- WordPress 5.0 or higher
- PHP 7.0 or higher

## 📝 Frequently Asked Questions

**Q: What happens if I don't create an "Organic Menu"?**  
A: The plugin will attempt to load the "Organic Menu", but if it doesn't exist, WordPress will fall back to the default menu behavior.

**Q: Can I customize the cookie duration?**  
A: Yes, you can modify the `$expiration_time` variable in the plugin code. Currently set to 30 days.

**Q: Does this work with custom theme locations?**  
A: Yes, the plugin checks both menu names and theme locations (specifically the 'primary' location).

**Q: Will this affect my site's performance?**  
A: No, the plugin is extremely lightweight and only performs simple string checks on each page load.

**Q: Can I track which menu is being displayed?**  
A: You can check for the `organic_user` cookie in your browser's developer tools to see if the organic menu should be displayed.

## 🛠️ Customization

To modify the browser detection or add additional browsers, edit the `check_organic_user()` function in the plugin file.

To change which menu is displayed for organic users, modify the menu name in the `change_menu()` function:

```php
$args['menu'] = 'Your Custom Menu Name';
```

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

## 📄 License

This plugin is licensed under the GPL v2 or later.

## 👨‍💻 Author

**Spaceo Tech**

## 📞 Support

For support, please open an issue in the GitHub repository or contact Spaceo Tech.

## 🔄 Changelog

### Version 1.0
- Initial release
- Browser detection functionality
- Cookie-based organic user tracking
- Automatic menu switching
- Support for theme locations and menu names

## 🙏 Credits

Developed by Spaceo Tech

---

**Note**: This plugin sets cookies. Ensure your website's privacy policy includes information about cookie usage to comply with GDPR and other privacy regulations.
