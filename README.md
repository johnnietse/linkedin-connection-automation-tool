# LinkedIn Connection Automation Tool

## Core Automation
![Selenium](https://img.shields.io/badge/Selenium-4.9.1-43B02A?logo=selenium)
![OpenCV](https://img.shields.io/badge/OpenCV-4.8.0.74-5C3EE8?logo=opencv)
![PyAutoGUI](https://img.shields.io/badge/PyAutoGUI-0.9.54-FFD43B)

## Data Processing
![Pandas](https://img.shields.io/badge/Pandas-2.0.3-150458?logo=pandas)
![OpenPyXL](https://img.shields.io/badge/OpenPyXL-3.1.2-217346?logo=openpyxl)

## Image Processing
![NumPy](https://img.shields.io/badge/NumPy-1.24.4-013243?logo=numpy)
![imutils](https://img.shields.io/badge/imutils-0.5.4-00A98F)
![Pillow](https://img.shields.io/badge/Pillow-10.0.0-8F00FF?logo=python)

## Environment & Utilities
![python-dotenv](https://img.shields.io/badge/python--dotenv-1.0.0-ECD53F)
![tqdm](https://img.shields.io/badge/tqdm-4.65.0-FF6F00)

## WebDriver Management
![webdriver-manager](https://img.shields.io/badge/webdriver--manager-3.8.6-00B7EB)

## ⚠️ Important Disclaimer ⚠️
After creating this LinkedIn automation program, I have come to realize and understand that LinkedIn explicitly prohibits the use of automation tools for activities on their platform unless these tools are developed through official partnerships with LinkedIn. Using unauthorized automation tools like this one may result in your LinkedIn account being permanently restricted or banned.

I am sharing this project on GitHub purely as a demonstration of my technical work. I strongly advise against using this tool for actual LinkedIn activities, as it violates LinkedIn's User Agreement (Section 8.2) and Professional Community Policies.

By accessing or using this software, you acknowledge that:
- You understand the risks of account restriction or permanent banning
- You take full responsibility for any consequences that may result from using this tool
- You agree not to use this tool for any commercial or large-scale automation
- LinkedIn's terms prohibit automation without explicit permission

Finally, the use of this tool to interact with LinkedIn may violate LinkedIn’s Terms of Service.
The author assumes no responsibility for any consequences arising from use of this tool.

## Overview
This Python-based tool automates sending connection requests on LinkedIn using a combination of:
- Selenium for browser automation
- OpenCV for image recognition
- Text scraping for button identification
- Excel for data management

The tool processes LinkedIn profile URLs from an Excel file and sends connection requests with "Send without a note".

## Features
- Hybrid identification system combining text scraping and image recognition
- State detection for "Message" and "Pending" statuses
- Excel integration for input and result tracking
- Anti-detection measures with randomized delays
- Progress saving with automatic Excel updates
- Multi-template support for different UI variations

## Requirements
- Python 3.8+
- Chrome browser
- ChromeDriver matching your Chrome version
- Required Python packages: `selenium`, `opencv-python`, `numpy`, `pandas`, `openpyxl`, `pyautogui`, `python-dotenv`

## Installation
```bash
# Clone the repository
git clone https://github.com/johnnietse/linkedin-connection-automation-tool.git

# Navigate to project directory
cd linkedin-connection-automation-tool

# Create a virtual environment:
python -m venv venv

```
- For Windows: 
```bash
venv\Scripts\activate 
```

- For Linux/Mac:
```bash
source venv/bin/activate
```


# Install required packages
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

## How to Download & Install ChromeDriver Correctly
1. Check Your Chrome Version
    1. Open Chrome
    2. Click ⋮ (Menu) → Help → About Google Chrome
    3. Note the full version number (e.g., 137.0.7151.56)

2. Download Matching ChromeDriver
Based on your Chrome version (ex. 137.0.7151.56). You will need to change this according to your Chrome version number:

```powershell
# For 64-bit Windows:
https://storage.googleapis.com/chrome-for-testing-public/137.0.7151.55/win64/chromedriver-win64.zip

# For 32-bit Windows:
https://storage.googleapis.com/chrome-for-testing-public/137.0.7151.55/win32/chromedriver-win32.zip
```
⚠️ Note: Your Chrome version (137.0.7151.56) uses ChromeDriver 137.0.7151.55 - they are compatible despite the minor difference. 

3. Installation Steps
    1. Download the correct ZIP file using the links above
    2. Extract the ZIP file
    3. Locate chromedriver.exe in the extracted files
    4. Place it in your project folder:

<pre>
linkedinConnectionAutomation/
│
├── data/
│   ├── input_profiles.xlsx
│   └── results.xlsx
│
├── templates/
│   ├── connect_button_1.png
│   ├── connect_button_2.png
│   ├── connect_button_3.png
│   ├── message_button_1.png
│   ├── message_button_2.png
│   ├── pending_button_1.png
│   ├── send_without_note_button_1.png
│   ├── send_without_note_button_2.png
│   └── send_without_note_button_3.png
│
├── LICENSE
├── README.md  
├── chromedriver.exe # <-- Place it here/Replace it with a version of ChromeDriver that can run the automation program with your Chrome Browser 
├── linkedin_follower.py
└── requirements.txt
</pre>

Note: 
- About the .venv Directory: 
When setting up this project in PyCharm (or any Python development environment), you will typically create a virtual environment, often named `.venv` or any other way you name it. This directory is intentionally excluded from the GitHub repository for important technical reasons. This is because Virtual Environments (.venv) contain platform-specific binaries that won't work for other users, and they are typically 100-500MB in size (too large for version control). Hence, they should always be recreated locally using `requirements.txt`.


## Configuration
1. Prepare templates:

- Add button images to `templates/` directory:
  - Connect buttons (3 variations)
  - Send without note buttons (3 variations)
  - Message buttons (2 variations)
  - Pending button (1 variation)

2. Set up credentials:
- Create .env file with your LinkedIn credentials (This feature no longer exists as Linkedin can track that you are logging in with an automation program):
```bash
LINKEDIN_EMAIL="your@email.com"
LINKEDIN_PASSWORD="yourpassword"
```

3. Prepare Excel file:
- Add LinkedIn profile URLs to `data/input_profiles.xlsx`
- First column should contain URLs

## Usage
```bash
python linkedin_connector.py
```

The program will:
1. Launch Chrome browser
2. Prompt you to complete login manually
3. Process profiles from Excel file
4. Save results to data/results.xlsx
5. Implement randomized delays between actions

## Ethical Considerations
While this tool demonstrates technical capabilities in automation, it's important to consider:
1. **Platform integrity**: Automation undermines LinkedIn's professional ecosystem
2. **User experience**: Automated connections devalue genuine networking
3. **Privacy concerns**: Mass automation violates others' expectations of consent
4. **Legal compliance**: Violates LinkedIn's Terms of Service

## Alternative Approaches
Instead of automation, consider these LinkedIn-approved methods:
1. **Official LinkedIn API**: For approved developers
2. **Sales Navigator**: LinkedIn's premium relationship management tool
3. **Partner integrations**: Tools like Salesforce, HubSpot, etc.
4. **Manual networking**: Authentic relationship building

## Contributing
This repository is for educational purposes only. Hence, I will not accept contributions that:
- Enhance automation capabilities
- Improve evasion of LinkedIn detection
- Increase scale or efficiency of automation

## License
This project is licensed under the MIT License - but again, I strongly discourage actual use of this tool on LinkedIn as it may get your account restricted permanently.

## Important Data Usage Notice
The two `.xlsx` files located in the [`data/`](data/) directory of this repository serve **exclusively as examples** to demonstrate:
1. How to structure your own spreadsheets for use with this tool
2. The required data & URLs format for LinkedIn URL processing
3. How to organize connection information for optimal parsing

**These example files are NOT FOR PUBLIC USAGE OR DISTRIBUTION.** They contain data & URLs generated solely for demonstration purposes. DO NOT USE for actual networking. 
Refer to [Professional Connections Master List](https://docs.google.com/spreadsheets/d/1fegEXTyBf1ROCOk5-09cY1s-Qh8UvBH-Ng3oZ4hP784/edit?gid=0#gid=0) for authorized connection sources.

For legitimate professional networking purposes and actual connection references:
→ **Always consult the official collaboration spreadsheet** because this tool operates using LinkedIn URLs **derived directly from this public networking spreadsheet:  
[Professional Connections Master List](https://docs.google.com/spreadsheets/d/1fegEXTyBf1ROCOk5-09cY1s-Qh8UvBH-Ng3oZ4hP784/edit?gid=0#gid=0)

### Key Guidelines:
1. Never share the example `.xlsx` files outside this repository
2. Never use the placeholder LinkedIn URLs for actual networking
3. **Verify permissions** before using any LinkedIn automation with public spreadsheets
4. **Comply with LinkedIn's Terms of Service** for automation tools
5. **Transparency notice** - All LinkedIn URLs used by the tool are publicly accessible through the spreadsheet above --> [Professional Connections Master List](https://docs.google.com/spreadsheets/d/1fegEXTyBf1ROCOk5-09cY1s-Qh8UvBH-Ng3oZ4hP784/edit?gid=0#gid=0)
6. **Compliance responsibility**:  
   - Users must ensure their automation activities comply with:
       - LinkedIn's User Agreement
       - Relevant privacy regulations 
       - Professional ethics standards
7. **Respect privacy** - only use publicly shared information with proper consent
8. Always replace sample data with your own verified information
9. Refer to the official Google Sheet for current connection details
10. **Replace sample data** with your own verified information when creating personal spreadsheets

## ⚠️ Professional Ethics Notice
The LinkedIn data in the public spreadsheet is shared for professional networking purposes.
- Respect connection preferences
- Never spam users

## Last Notice

Again, this repository is shared strictly as a demonstration of technical capabilities and workflow design. We highly recommend against using this tool for actual LinkedIn automation. This is because:
- Actual implementation may:
   - Violate LinkedIn's Terms of Service
   - Risk account suspension or banning
   - Potentially damage professional relationships

- Automation of networking activities:
   - May be perceived as inauthentic or spammy
   - Could undermine genuine professional connections
   - Raises privacy considerations
 
### Liability Notice 
   Again, 
   - The authors accept no responsibility for any consequences of using this code
   - Users implement this technology entirely at their own risk
     

