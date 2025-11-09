# PinTips ZeppOS Project Structure Guide

## Recommended Directory Structure

When uploading your PinTips project files, organize them according to this structure:

```
PinTipsZeppOS/
├── README.md                    # Project overview and documentation
├── CONTRIBUTING.md              # How to contribute
├── .gitignore                   # Files to exclude from Git
│
├── app.json                     # App manifest and configuration
├── app.js                       # App lifecycle management
│
├── page/                        # Application pages
│   ├── index.js                # Main page logic
│   ├── index.style.js          # Page styles
│   └── settings.js             # Settings page (if applicable)
│
├── assets/                      # Static resources
│   ├── images/                 # Image assets
│   │   ├── icon.png           # App icon
│   │   └── screenshots/       # App screenshots
│   ├── fonts/                  # Custom fonts
│   └── raw/                    # Other raw assets
│
├── utils/                       # Utility functions
│   ├── index.js                # Utility exports
│   ├── storage.js              # Local storage helpers
│   └── api.js                  # API interactions
│
└── package.json                 # Node.js dependencies (if any)
```

## File Descriptions

### app.json
The app manifest file containing:
- App metadata (name, version, description)
- Target devices and screen configurations
- Permissions and capabilities
- Page routing configuration

Example structure:
```json
{
  "app": {
    "appId": "com.example.pintips",
    "appName": "PinTips",
    "appType": "app",
    "version": {
      "code": 1,
      "name": "1.0.0"
    }
  },
  "permissions": [],
  "runtime": {
    "apiVersion": {
      "compatible": "1.0.0",
      "target": "1.0.1"
    }
  },
  "targets": {
    "defaultTarget": "480x480-round"
  },
  "i18n": {
    "en-US": {
      "appName": "PinTips"
    }
  },
  "defaultLanguage": "en-US"
}
```

### app.js
App lifecycle management:
```javascript
App({
  globalData: {},
  onCreate(options) {
    console.log('App onCreate')
  },
  onDestroy(options) {
    console.log('App onDestroy')
  }
})
```

### page/index.js
Main page logic:
```javascript
Page({
  build() {
    console.log('Page build')
  },
  onInit() {
    console.log('Page onInit')
  },
  onDestroy() {
    console.log('Page onDestroy')
  }
})
```

## Before Uploading

### Checklist
- [ ] Remove any sensitive data (API keys, passwords)
- [ ] Remove `node_modules/` if present
- [ ] Include a README.md with project description
- [ ] Verify app.json configuration is correct
- [ ] Test that your app builds and runs
- [ ] Add appropriate .gitignore entries

### File Size Considerations
- ZeppOS apps have size limitations
- Optimize images before uploading
- Use appropriate image formats (PNG for transparency, JPG for photos)
- Consider compressing assets

### Code Quality
- Use consistent code formatting
- Add comments for complex logic
- Follow ZeppOS best practices
- Handle errors appropriately

## Next Steps After Upload

1. **Set up CI/CD** (if needed)
   - Automated testing
   - Build automation
   - Deployment pipeline

2. **Documentation**
   - Update README with specific features
   - Document API usage
   - Add user guide

3. **Testing**
   - Test on simulator
   - Test on real devices
   - Document device compatibility

4. **Release Process**
   - Version management
   - Changelog maintenance
   - Release notes

## References

- [ZeppOS Developer Guide](https://docs.zepp.com/docs/intro/)
- [ZeppOS API Documentation](https://docs.zepp.com/docs/reference/)
- [ZeppOS Simulator](https://docs.zepp.com/docs/guides/tools/simulator/)
- [ZeppOS Best Practices](https://docs.zepp.com/docs/guides/best-practice/)

## Questions?

If you need help with the project structure or uploading your files:
1. Check the [CONTRIBUTING.md](CONTRIBUTING.md) guide
2. Review the ZeppOS documentation
3. Open an issue for specific questions
