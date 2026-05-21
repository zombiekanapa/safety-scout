# Safety Scout - Free & Open-Source Edition

**Civilian safety analysis powered by Hugging Face & GitHub Pages**

## 🚀 Quick Start

### Option 1: Use Published Version
Already deployed! Just visit:
- **Frontend**: `https://yourusername.github.io/safety-scout`
- **Backend**: `https://yourusername-safety-scout.hf.space`

### Option 2: Deploy Yourself (5 minutes)

#### Frontend (GitHub Pages)
1. **Fork this repo** → `Settings` → `Pages`
2. **Enable GitHub Pages** → Source: `main` branch
3. Done! Your app is live at `https://yourusername.github.io/safety-scout`

#### Backend (Hugging Face Spaces)
1. **Go to** [huggingface.co/spaces](https://huggingface.co/spaces)
2. **Create New Space** → Select "Gradio" (Python) → Paste `hf-spaces-backend.py`
3. **Done!** Copy the Space URL into app settings

## 📊 Architecture

```
User's Browser (GitHub Pages)
        ↓
    index.html (17KB optimized)
        ↓
 Calls HF Spaces API
        ↓
HF Spaces Backend (Free)
        ↓
Vision Transformer (image detection)
Text Model (analysis generation)
        ↓
    JSON Response
        ↓
  Results displayed
```

## ✨ Features

✅ **100% Free** - No API keys, no credit cards  
✅ **Open Source** - MIT licensed, fork & modify  
✅ **Privacy First** - Images processed, never stored  
✅ **Bilingual** - English & Polish  
✅ **Offline Mode** - ONNX local model support (coming)  
✅ **Mobile Ready** - Progressive Web App  

## 📁 Files

| File | Purpose | Size |
|------|---------|------|
| `index-optimized.html` | Complete frontend app | 22KB |
| `hf-spaces-backend.py` | Hugging Face Spaces backend | 6KB |
| `deploy.yml` | GitHub Actions workflow | 1KB |
| `README.md` | This file | - |

## 🎯 How It Works

### Safety Scan Mode
- Analyzes image for fire, medical, electrical hazards
- Detects objects using Vision Transformer
- Generates recommendations using Flan-T5
- Returns structured report

### Fire Drill Mode
- Creates 60-second emergency scenarios
- Defines civilian goals and safety checklists
- Helps practice evacuation procedures

## 🔧 Setup Steps

### 1. Prepare Frontend
```bash
# Clone or fork repo
git clone https://github.com/yourusername/safety-scout.git
cd safety-scout

# Rename optimized version
mv index-optimized.html index.html

# Push to GitHub
git add .
git commit -m "Initial commit"
git push origin main
```

### 2. Enable GitHub Pages
1. Go to repo **Settings**
2. Select **Pages** (left sidebar)
3. Source: **main branch**
4. Save

Your frontend is now live! 🎉

### 3. Deploy Backend to HF Spaces

**Option A: Simple (No coding)**
1. Go to [huggingface.co/spaces/create](https://huggingface.co/spaces/create)
2. Space name: `civilian-safety` (or any name)
3. Space type: **Gradio**
4. Copy entire `hf-spaces-backend.py` into `app.py`
5. Click "Create Space"
6. Copy your Space URL: `https://username-space.hf.space`

**Option B: With CLI (Advanced)**
```bash
huggingface-cli repo create civilian-safety --type space --space-sdk gradio
cd civilian-safety
cp hf-spaces-backend.py app.py
git add .
git commit -m "Initial setup"
git push
```

### 4. Update App Settings
In the deployed app:
1. Click ⚙️ (Settings)
2. Paste your HF Space URL
3. Click "SAVE & COMMIT"

**Done!** 🚀

## 💡 Advanced Usage

### Custom Models
Edit `hf-spaces-backend.py`:
```python
# Use different models from Hugging Face Hub
vision_model = pipeline("image-classification",
    model="microsoft/resnet-50")  # Change this
```

### Local ONNX Mode (Offline)
Coming soon! App supports local ONNX models for fully offline use.

### Environment Variables
```bash
# In HF Spaces settings
HF_TOKEN=your_token_here
MODEL_SIZE=small  # or 'large' for more accuracy
```

## 🌍 Supported Languages
- 🇬🇧 English
- 🇵🇱 Polish (Język Polski)

## 📊 Performance

| Metric | Value |
|--------|-------|
| Frontend Size | 22 KB (minified) |
| Load Time | < 2s (CDN cached) |
| Analysis Time | 5-30s (depends on HF queue) |
| Free API Calls | ∞ (HF Spaces) |
| Storage | ∞ (GitHub + HF) |

## 🔒 Privacy & Security

- ✅ **No data collection** - Images processed in-memory only
- ✅ **No tracking** - No analytics, no cookies
- ✅ **Open source** - Audit the code yourself
- ✅ **HTTPS only** - Secure communication
- ✅ **Stateless** - Nothing stored between requests

## 🐛 Troubleshooting

### "HF Spaces API not responding"
- Check Space is running: visit URL directly
- Try restarting Space: Organizers → Restart

### "Image upload fails"
- Check file size (< 10MB recommended)
- Try JPG instead of PNG
- Clear browser cache (Ctrl+Shift+Delete)

### "Results look generic"
- Models may need fine-tuning for your use case
- Consider training custom model on your data
- Contribute improvements to repo!

## 🤝 Contributing

Found a bug? Have an idea? **Help improve Safety Scout!**

1. Fork the repo
2. Create feature branch: `git checkout -b feature/amazing-thing`
3. Commit: `git commit -am 'Add amazing thing'`
4. Push: `git push origin feature/amazing-thing`
5. Open Pull Request

## 📚 Resources

- [Hugging Face Docs](https://huggingface.co/docs)
- [GitHub Pages Guide](https://pages.github.com)
- [Vision Transformers](https://huggingface.co/google/vit-base-patch16-224)
- [Flan-T5 Models](https://huggingface.co/google/flan-t5-small)

## 📝 License

MIT License - Free to use, modify, and distribute

## 🙋 Support

- **GitHub Issues**: Report bugs & request features
- **Discussions**: Ask questions and share ideas
- **HF Community**: [safety-scout-tag](https://huggingface.co)

## 🎓 Educational Use

Perfect for:
- 🏫 Safety training courses
- 🚒 Fire department drills
- 🏢 Workplace safety programs
- 👨‍👩‍👧‍👦 Community emergency preparedness

---

**Made with ❤️ for civilian safety by the community**

No API keys. No charges. No bullshit. Just safety.
