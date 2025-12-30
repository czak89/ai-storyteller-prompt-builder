# Installation & Setup Guide

## 🚀 Quick Start (Recommended)

The AI Story Writing Prompt Builder is a **standalone web application** that requires no installation or server setup.

### **Option 1: Direct Download & Open**
1. Download `ai-prompt-builder-enhanced-ux.html`
2. Double-click the file to open in your default browser
3. Start creating prompts immediately!

### **Option 2: Save & Bookmark**
1. Save the HTML file to your preferred location (e.g., Desktop, Documents)
2. Open in your browser and bookmark for easy access
3. Works offline after first load!

---

## 🌐 Browser Requirements

### **Minimum Requirements**
- **Chrome**: Version 90+ (Recommended)
- **Firefox**: Version 88+
- **Safari**: Version 14+
- **Edge**: Version 90+

### **For WebLLM AI Features**
- **Chrome/Edge**: Version 113+ with WebGPU enabled
- **Hardware**: Modern GPU (integrated graphics sufficient)
- **Memory**: 4GB+ RAM recommended for larger models

### **Mobile Support**
- **iOS Safari**: 14+
- **Android Chrome**: 90+
- **Responsive design** works on all screen sizes

---

## ⚙️ Configuration Options

### **WebLLM Setup (Browser AI)**
1. Select a model from the dropdown
2. First load will download the model (2-4GB)
3. Subsequent uses are instant and offline
4. **No API keys required!**

**Recommended Models:**
- **Llama 3.2 1B**: Fast, 2GB download
- **Llama 3.2 3B**: Better quality, 4GB download
- **Phi 3.5 Mini**: Efficient, 2GB download

### **OpenAI API Setup**
1. Get API key from [OpenAI Platform](https://platform.openai.com)
2. Enter key in the OpenAI tab
3. Select your preferred model
4. **Keys stored locally only**

### **Custom Endpoint Setup**
**For Ollama:**
1. Install [Ollama](https://ollama.ai)
2. Run: `ollama serve`
3. Click "Ollama" preset in the app
4. Click "Discover Models"

**For LM Studio:**
1. Install [LM Studio](https://lmstudio.ai)
2. Start local server
3. Click "LM Studio" preset
4. Discover available models

---

## 🔧 Advanced Setup

### **Local Development**
If you want to modify the code:

```bash
# Clone or download the files
git clone [repository-url]

# Open in your preferred editor
code ai-prompt-builder-enhanced-ux.html

# Open in browser for testing
open ai-prompt-builder-enhanced-ux.html
```

### **Web Server Deployment**
For team use or web hosting:

```bash
# Simple Python server
python -m http.server 8000

# Node.js server
npx serve .

# Access at http://localhost:8000
```

### **Customization**
The application supports customization through:
- **CSS Variables**: Easy theme modifications
- **LocalStorage**: Persistent user preferences
- **Modular JavaScript**: Easy feature additions

---

## 🛠️ Troubleshooting

### **Common Issues**

**WebLLM Not Loading:**
- Ensure Chrome/Edge with WebGPU support
- Check available disk space (4GB+ needed)
- Try a smaller model first (Llama 3.2 1B)
- Clear browser cache and reload

**OpenAI API Errors:**
- Verify API key is correct
- Check account has credits
- Ensure model access permissions
- Try different model if rate limited

**Custom Endpoint Issues:**
- Verify endpoint URL is correct
- Check if service is running
- Test with curl: `curl http://localhost:11434/v1/models`
- Ensure CORS is enabled on server

**Layout Issues:**
- Try different browser
- Clear browser cache
- Disable browser extensions
- Check console for JavaScript errors

### **Performance Optimization**

**For Better Performance:**
- Use Chrome or Edge for best WebLLM support
- Close other browser tabs when using WebLLM
- Ensure adequate RAM (4GB+ recommended)
- Use SSD storage for faster model loading

**For Mobile Devices:**
- Use smaller WebLLM models (1B parameters)
- Consider OpenAI API for better mobile performance
- Ensure stable internet connection
- Close other apps to free memory

---

## 📱 Platform-Specific Notes

### **Windows**
- Works with all modern browsers
- WebLLM requires Windows 10+ with DirectX 12
- Edge often performs better than Chrome for WebLLM

### **macOS**
- Safari works well for basic features
- Chrome recommended for WebLLM
- M1/M2 Macs excellent for WebLLM performance

### **Linux**
- Chrome/Firefox both work well
- May need to enable WebGPU flags manually
- Check GPU drivers for WebLLM support

### **iOS**
- Safari works for all features except WebLLM
- Use OpenAI API or custom endpoints for AI features
- Responsive design optimized for touch

### **Android**
- Chrome recommended
- WebLLM may work on high-end devices
- Consider API-based solutions for better performance

---

## 🔐 Privacy & Security

### **Data Storage**
- **Local Only**: All data stored in browser localStorage
- **No Tracking**: No analytics or data collection
- **No Server**: Completely client-side application
- **Secure**: API keys never leave your browser

### **API Key Security**
- Keys stored in browser localStorage only
- Never transmitted except to chosen AI service
- Clear browser data to remove keys
- Use environment-specific keys for development

### **Offline Usage**
- Works completely offline after initial load
- WebLLM models cached locally
- Recent prompts and preferences saved locally
- No internet required for core functionality

---

## 📞 Support

### **Getting Help**
- Check browser console for error messages
- Try different browser or incognito mode
- Clear browser cache and localStorage
- Ensure JavaScript is enabled

### **Feature Requests**
- The application is designed to be self-contained
- Most customizations can be done through CSS variables
- Consider forking for major modifications

### **Compatibility Issues**
- Test with latest browser versions
- Check WebGPU support at [webgpureport.org](https://webgpureport.org)
- Verify hardware meets minimum requirements
- Try different AI providers if one fails

---

## 🎯 Next Steps

After installation:
1. **Explore Templates**: Try the preset templates for quick start
2. **Test AI Integration**: Set up your preferred AI provider
3. **Customize Settings**: Adjust font size and theme preferences
4. **Create Your First Prompt**: Use the guided workflow
5. **Export & Save**: Try the export features for backup

The application is designed to work immediately without configuration, but these setup options provide enhanced functionality and customization for power users.