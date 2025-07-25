# MG Car Configurator - Unity WebGL Template

This is a custom Unity WebGL template designed specifically for the MG Car Configurator project. It provides a professional, branded interface with optimized performance and user experience.

## Features

### 🎨 MG Branding
- Custom MG logo integration (white and red variants)
- Brand-consistent color scheme (MG Red #D32F2F, Black #1A1A1A)
- Professional typography using Inter font family
- Responsive design for all devices

### ⚡ Performance Optimizations
- Progressive loading with branded loading screen
- Adaptive quality settings modal
- Mobile-optimized touch controls
- Performance monitoring and analytics
- Memory-efficient asset loading

### 🎮 Interactive Features
- **Keyboard Shortcuts:**
  - `1-7`: Quick material switching
  - `R`: Reset camera position
  - `F`: Toggle fullscreen mode
- **Mouse Controls:**
  - Mouse wheel: Zoom in/out
  - Right-click drag: Pan camera
  - Left-click drag: Orbit camera
- **Touch Controls:**
  - Single finger: Orbit camera
  - Two fingers: Pan and zoom

### 🔧 Quality Settings
- Ultra: Maximum quality for high-end desktops
- High: Balanced quality for standard desktops
- Medium: Optimized for tablets and mid-range devices
- Low: Performance mode for mobile and weak devices

## Installation

1. **Copy Template**: The template is already installed in `Assets/WebGLTemplates/MG-Configurator/`

2. **Select Template in Unity**:
   - Go to `File > Build Settings`
   - Select `WebGL` platform
   - Click `Player Settings`
   - Under `Publishing Settings`, set `WebGL Template` to `MG-Configurator`

3. **Build Project**:
   - Choose your build folder
   - Click `Build` or `Build and Run`

## File Structure

```
Assets/WebGLTemplates/MG-Configurator/
├── index.html              # Main template file with Unity integration
├── TemplateData/
│   ├── style.css           # MG-branded styles and responsive design
│   ├── mg-logo-white.png   # MG logo for header
│   ├── mg-logo-red.png     # MG logo for loading screen
│   └── favicon.ico         # Website favicon
└── README.md               # This documentation
```

## Customization

### Colors
Edit the CSS variables in `TemplateData/style.css`:
```css
:root {
    --mg-red: #D32F2F;        /* Primary MG red */
    --mg-dark-red: #B71C1C;   /* Darker red for hover states */
    --mg-black: #1A1A1A;      /* Primary dark color */
    --mg-white: #FFFFFF;      /* Primary light color */
    --mg-gold: #FFD700;       /* Accent color for progress bars */
}
```

### Loading Tips
Modify the `loadingTips` array in `index.html`:
```javascript
var loadingTips = [
    "💡 Use mouse wheel to zoom, right-click to pan",
    "🎨 Press 1-7 to quickly change materials",
    // Add your custom tips here
];
```

### Unity Integration
The template automatically integrates with your Unity scripts:
- `CarMaterialSwapper.cs` - Material switching functionality
- `CameraOrbit.cs` - Camera control system
- `QualitySettings` - Graphics quality management

## Browser Compatibility

### Desktop
- ✅ Chrome 80+
- ✅ Firefox 75+
- ✅ Safari 13+
- ✅ Edge 80+

### Mobile
- ✅ iOS Safari 13+
- ✅ Android Chrome 80+
- ✅ Samsung Internet 12+

## Performance Recommendations

### For Best Performance:
1. **Texture Optimization**: Use compressed textures (DXT5/BC7 for desktop, ASTC for mobile)
2. **Model Optimization**: Keep polygon count under 50k triangles
3. **Memory Settings**: Use 64MB initial, 1024MB maximum WebGL memory
4. **Compression**: Enable Brotli compression in Unity build settings

### Quality Settings Mapping:
- **Ultra (0)**: Full quality, all effects enabled
- **High (1)**: High quality with reduced shadows
- **Medium (2)**: Balanced quality, some effects disabled
- **Low (3)**: Performance mode, minimal effects

## Troubleshooting

### Common Issues:

**Template not showing in Unity:**
- Ensure the template folder is in `Assets/WebGLTemplates/`
- Restart Unity Editor
- Check that all files are present

**Loading errors:**
- Verify Unity build files are in the correct `Build/` folder
- Check browser console for specific error messages
- Ensure all template assets are properly copied

**Performance issues:**
- Lower the quality setting using the in-app modal
- Check that textures are properly compressed
- Monitor memory usage in browser dev tools

## Development

### Testing Locally:
1. Build your Unity project to a local folder
2. Serve the files using a local web server (not file:// protocol)
3. Test on multiple devices and browsers

### Deployment:
1. Upload all build files to your web server
2. Ensure proper MIME types for `.wasm` and `.data` files
3. Enable compression (Gzip/Brotli) on your server
4. Test loading performance and functionality

## Support

For issues specific to this template:
1. Check the browser console for error messages
2. Verify Unity WebGL build settings match recommendations
3. Test with a fresh Unity WebGL build
4. Ensure all MG logo assets are properly copied

## Version History

- **v1.0** - Initial MG-branded template with full feature set
- Responsive design and mobile optimization
- Quality settings modal and keyboard shortcuts
- Performance monitoring and error handling
