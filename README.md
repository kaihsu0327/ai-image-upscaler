# AI Image Upscaler 🚀

A powerful desktop application for upscaling images using AI-powered Real-ESRGAN technology. Built with Python and Tkinter for a clean, user-friendly interface.

![Version](https://img.shields.io/badge/version-1.0-blue)
![Python](https://img.shields.io/badge/python-3.8+-green)
![License](https://img.shields.io/badge/license-MIT-orange)

## ✨ Features

- 🎨 **GUI Interface** - Clean and intuitive design
- 🤖 **AI-Powered Upscaling** - Uses Real-ESRGAN for high-quality image enhancement
- 📊 **Multiple Scale Options** - 2x, 3x, and 4x upscaling
- 🎭 **Multiple AI Models** - Choose from different models optimized for photos or anime
- 📁 **Batch Processing** - Upscale multiple images at once
- 📈 **Real-time Progress** - Animated progress bar with status updates
- 💾 **Format Support** - PNG, JPG, WEBP, BMP output formats
- ⚡ **GPU Acceleration** - Utilizes NVIDIA GPU for faster processing

## 🖼️ Screenshots

*Add screenshots of your application here*

## 📋 Requirements

- Windows 10 or later
- NVIDIA GPU (optional but recommended for faster processing)
- 4GB RAM minimum

## 🚀 Installation

### Option 1: Download Pre-built Executable (Recommended)

1. Download the latest release from [Releases](https://github.com/ChamikaSamaraweera/ai-image-upscaler/releases)
2. Extract the ZIP file
3. Run `AIImageUpscaler.exe`

### Option 2: Build from Source

1. **Clone the repository**
```bash
git clone https://github.com/ChamikaSamaraweera/ai-image-upscaler.git
cd ai-image-upscaler
```

2. **Install Python dependencies**
```bash
pip install -r requirements.txt
```

3. **Download Real-ESRGAN**
   - Download from [Real-ESRGAN Releases](https://github.com/xinntao/Real-ESRGAN/releases)
   - Extract `realesrgan-ncnn-vulkan.exe` to the project root
   - Extract the `models` folder to the project root

4. **Run the application**
```bash
python app.py
```

## 🔨 Building the Executable

To build your own executable:

```bash
pyinstaller --onefile --noconsole --windowed --add-binary="realesrgan-ncnn-vulkan.exe;." --add-data="models;models" --add-data="icon.ico;." --icon=icon.ico --name="AIImageUpscaler" app.py
```

The executable will be created in the `dist` folder.

## 📖 Usage

1. **Select Images**: Click "📁 Browse Images" to select one or more images
2. **Choose Output Location**: Click "📂 Select Output Folder" (optional - defaults to source folder)
3. **Configure Settings**:
   - Select AI Model (General, Anime, or AnimeVideo)
   - Choose Upscale Factor (2x, 3x, or 4x)
   - Select Output Format (PNG, JPG, or WEBP)
4. **Start Processing**: Click "Upscale Button" to begin
5. **Wait for Completion**: Monitor progress bar and status messages

## 🎯 AI Models

| Model | Best For | Available Scales |
|-------|----------|------------------|
| `realesrgan-x4plus` | General photos and realistic images | 2x, 3x, 4x |
| `realesrgan-x4plus-anime` | Anime and illustrated content | 2x, 3x, 4x |
| `realesr-animevideov3` | Anime videos and animation | 2x, 3x, 4x |
| `realesrnet-x4plus` | General purpose | 4x only |

## 📁 Project Structure

```
ai-image-upscaler/
├── app.py                          # Main application file
├── icon.ico                        # Application icon
├── realesrgan-ncnn-vulkan.exe     # Real-ESRGAN executable
├── models/                         # AI model files
│   ├── realesrgan-x4plus.bin
│   ├── realesrgan-x4plus.param
│   └── ... (other model files)
├── requirements.txt                # Python dependencies
└── README.md                       # This file
```

## 🛠️ Technologies Used

- **Python 3.8+** - Core programming language
- **Tkinter** - GUI framework
- **Pillow (PIL)** - Image processing
- **Real-ESRGAN** - AI upscaling engine
- **PyInstaller** - Executable building

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 Requirements.txt

```
Pillow>=10.0.0
```

## 🐛 Known Issues

- Console window may briefly appear during processing (working on fix)
- Large images (>4K) may take several minutes to process
- GPU memory limitations may affect very large batch processing

## 🔮 Future Enhancements

- [ ] Drag and drop support
- [ ] Image preview before/after
- [ ] Custom output filename patterns
- [ ] Queue management for large batches
- [ ] Support for more AI models
- [ ] Multi-language support

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) by Xintao Wang - For the amazing AI upscaling technology
- All contributors who help improve this project

## 👨‍💻 Developer

**Chamika Samaraweera**

- GitHub: [@ChamikaSamaraweera](https://github.com/ChamikaSamaraweera)
- Email: chamika@teaminfinity.lk

## ⭐ Support

If you find this project useful, please consider giving it a star on GitHub!

---

**Note**: This application uses Real-ESRGAN technology. Please refer to the [Real-ESRGAN license](https://github.com/xinntao/Real-ESRGAN/blob/master/LICENSE) for usage terms.