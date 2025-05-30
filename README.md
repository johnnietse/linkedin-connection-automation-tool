# LinkedIn Connection Automation Tool
Python
Selenium
OpenCV

⚠️ Important Legal Disclaimer ⚠️
After creating this LinkedIn automation program, I've come to understand that LinkedIn explicitly prohibits the use of automation tools for activities on their platform unless these tools are developed through official partnerships with LinkedIn. Using unauthorized automation tools like this one may result in your LinkedIn account being permanently restricted or banned.

I'm sharing this project on GitHub purely as a demonstration of my technical work and for educational purposes. I strongly advise against using this tool for actual LinkedIn activities, as it violates LinkedIn's User Agreement (Section 8.2) and Professional Community Policies.

By accessing or using this software, you acknowledge that:

You understand the risks of account restriction or permanent banning

You take full responsibility for any consequences that may result from using this tool

You agree not to use this tool for any commercial or large-scale automation

LinkedIn's terms prohibit automation without explicit permission

Overview
This Python-based tool automates sending connection requests on LinkedIn using a combination of:

Selenium for browser automation

OpenCV for image recognition

Text scraping for button identification

Excel for data management

The tool processes LinkedIn profile URLs from an Excel file and sends connection requests with "Send without a note".

Features
Hybrid identification system combining text scraping and image recognition

State detection for "Message" and "Pending" statuses

Excel integration for input and result tracking

Anti-detection measures with randomized delays

Progress saving with automatic Excel updates

Multi-template support for different UI variations

Requirements
Python 3.8+

Chrome browser

ChromeDriver matching your Chrome version

Required Python packages: selenium, opencv-python, numpy, pandas, openpyxl, pyautogui, python-dotenv

Installation
bash
# Clone the repository
git clone https://github.com/yourusername/linkedin-connection-automation.git

# Navigate to project directory
cd linkedin-connection-automation

# Install required packages
pip install -r requirements.txt
Configuration
Prepare templates:

Add button images to templates/ directory:

Connect buttons (3 variations)

Send without note buttons (3 variations)

Message buttons (2 variations)

Pending button (1 variation)

Set up credentials:

Create .env file with your LinkedIn credentials:

LINKEDIN_EMAIL="your@email.com"
LINKEDIN_PASSWORD="yourpassword"
Prepare Excel file:

Add LinkedIn profile URLs to data/input_profiles.xlsx

First column should contain URLs

Usage
bash
python linkedin_connector.py
The program will:

Launch Chrome browser

Prompt you to complete login manually

Process profiles from Excel file

Save results to data/results.xlsx

Implement randomized delays between actions

Ethical Considerations
While this tool demonstrates technical capabilities in automation, it's important to consider:

Platform integrity: Automation undermines LinkedIn's professional ecosystem

User experience: Automated connections devalue genuine networking

Privacy concerns: Mass automation violates others' expectations of consent

Legal compliance: Violates LinkedIn's Terms of Service

Alternative Approaches
Instead of automation, consider these LinkedIn-approved methods:

Official LinkedIn API: For approved developers

Sales Navigator: LinkedIn's premium relationship management tool

Partner integrations: Tools like Salesforce, HubSpot, etc.

Manual networking: Authentic relationship building

Contributing
This repository is for educational purposes only. I will not accept contributions that:

Enhance automation capabilities

Improve evasion of LinkedIn detection

Increase scale or efficiency of automation

License
This project is licensed under the MIT License - but again, I strongly discourage actual use of this tool on LinkedIn.

