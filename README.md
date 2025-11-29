# 🤖 Android Test Case Generator

A sleek PyQt6 application that generates comprehensive test cases for Android mobile applications using Google's Gemini AI. Simply provide screenshots or documents, and let AI create detailed, actionable test cases.

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![PyQt6](https://img.shields.io/badge/PyQt6-6.6+-green.svg)
![Gemini](https://img.shields.io/badge/Gemini-AI-orange.svg)
![Version](https://img.shields.io/badge/Version-2.0.0-purple.svg)

## ✨ Features

- **📷 Image Analysis**: Upload Android app screenshots for visual UI analysis
- **📄 Document Processing**: Import requirements from PDF, DOCX, or TXT files
- **🔗 Combined Input**: Use both image and document together for comprehensive analysis
- **🎛️ Input Mode Selector**: Easy switch between Image Only, Document Only, or Combined modes
- **🎯 Multiple Test Types**: Generate functional, UI/UX, integration, performance, security, and accessibility tests
- **📋 Copy to Clipboard**: One-click copy of generated test cases
- **💾 Export Options**: Save test cases as Markdown, TXT, or JSON
- **🎨 Modern UI**: Cyberpunk-inspired dark theme with neon accents

## 🚀 Quick Start

### 1. Get a Gemini API Key

1. Go to [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Create a new API key
3. Copy the key for use in the app

### 2. Install Dependencies

```bash
# Navigate to the project directory
cd /Users/admin/Desktop/projects/test

# Create a virtual environment (recommended)
python3 -m venv venv
source venv/bin/activate  # On macOS/Linux
# OR
venv\Scripts\activate  # On Windows

# Install dependencies
pip install -r requirements.txt
```

### 3. Run the Application

```bash
python main.py
```

## 📖 Usage

### Input Modes

The application offers three input modes for flexibility:

| Mode | Icon | Description | Best For |
|------|------|-------------|----------|
| **Image Only** | 📷 | Analyze app screenshots | Quick UI testing, visual inspection |
| **Document Only** | 📄 | Parse requirement documents | Spec-based testing, feature coverage |
| **Combined** | 🔗 | Use both image + document | Comprehensive testing, full coverage |

### Basic Workflow

1. **Enter API Key**: Paste your Gemini API key in the header field
2. **Select Input Mode**: Choose from Image Only, Document Only, or Combined
3. **Upload Input**:
   - Drag & drop files onto the drop zones
   - Or click to browse and select files
4. **Configure Options**:
   - Select test type (Comprehensive, Functional, UI/UX, etc.)
   - Add app context for better results (e.g., "Login screen", "Shopping cart")
5. **Generate**: Click the "⚡ GENERATE TEST CASES" button
6. **Export**: Copy to clipboard or save as MD/TXT/JSON

### Supported File Formats

| Type | Supported Formats | Notes |
|------|-------------------|-------|
| Image | PNG, JPG, JPEG, GIF, BMP | App screenshots, mockups |
| Document | PDF, DOCX, TXT, MD | Requirements, specifications |

### Test Types Explained

- **Comprehensive**: All test types combined (recommended)
- **Functional**: Core feature and workflow testing
- **UI/UX**: Visual elements and user experience
- **Integration**: Component interaction testing
- **Performance**: Load and response time testing
- **Security**: Authentication and data protection
- **Accessibility**: WCAG compliance testing

## 🔧 Environment Variables

You can set your API key as an environment variable to avoid entering it each time:

```bash
# Add to ~/.zshrc or ~/.bashrc
export GEMINI_API_KEY="your-api-key-here"
```

## 📁 Project Structure

```
test/
├── main.py           # Main application (PyQt6)
├── requirements.txt  # Python dependencies
├── README.md         # This file
└── venv/             # Virtual environment (after setup)
```

## 🎨 UI Theme

The application features a custom cyberpunk/neon theme:
- Dark gradient background (#0a0a0f → #12121a)
- Cyan accent (#00ffd5) for primary actions
- Pink accent (#ff6b9d) for secondary elements
- Monospace typography (JetBrains Mono, Fira Code)
- Smooth hover transitions and glow effects

## 📋 Generated Test Case Format

Test cases are generated in a structured format:

```markdown
## Test Suite: [Feature/Screen Name]

### Test Case TC-001: [Title]
**Priority:** High/Medium/Low
**Type:** Functional/UI/Integration/etc.
**Preconditions:**
- [Prerequisites]

**Test Steps:**
1. [Step 1]
2. [Step 2]

**Expected Results:**
- [Expected outcome]

**Automation Notes:** [Hints for automation]
```

## 🐛 Troubleshooting

### Common Issues

**"API Key Invalid" Error**
- Verify your API key at [Google AI Studio](https://makersuite.google.com/app/apikey)
- Ensure the key has Gemini API access enabled
- Check for extra whitespace when copying the key

**"ModuleNotFoundError"**
- Run `pip install -r requirements.txt` again
- Ensure you're in the correct virtual environment
- Try `pip install PyQt6 google-generativeai Pillow PyPDF2 python-docx`

**Image Not Loading**
- Check the file format (PNG, JPG, JPEG, GIF, BMP only)
- Verify the file isn't corrupted
- Try resizing very large images

**PDF Reading Issues**
- Ensure the PDF contains extractable text (not scanned images)
- Try a simpler PDF or convert to TXT
- For scanned documents, use OCR first

**Window Not Appearing**
- Check terminal for error messages
- Ensure PyQt6 is properly installed
- On macOS, you may need to grant Terminal accessibility permissions

## 📜 License

MIT License - Feel free to use and modify!

## 🙏 Credits

- [Google Gemini AI](https://deepmind.google/technologies/gemini/) - AI backbone
- [PyQt6](https://www.riverbankcomputing.com/software/pyqt/) - GUI framework
- [Pillow](https://pillow.readthedocs.io/) - Image processing
- [PyPDF2](https://pypdf2.readthedocs.io/) - PDF processing
- [python-docx](https://python-docx.readthedocs.io/) - DOCX processing
