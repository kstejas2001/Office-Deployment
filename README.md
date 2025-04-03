# Office-Deployment
This repository contains the Office Deployment Tool and a pre-configured XML file for installing Microsoft Office. The XML file specifies edition, language, and installation options. Follow the instructions to deploy Office easily.

## Contents
- setup.exe - The Office Deployment Tool.
- configuration.xml - Configuration file for Office installation.

## Usage
To install Office, download the files and follow the instructions.

## Installation Guide

### 1. Download the Repository
Clone this repository to your PC using Git:
  -->git clone https://github.com/kstejas2001/Office-Deployment.git
Or manually download the files by clicking Code → Download ZIP.

### 2. Run the Deployment Tool
1. Open Command Prompt (cmd) and navigate to the folder:
  -->cd C:\Path\To\Office\Deployment\Tool
2. Download the Office installation files:
  -->setup.exe /download configuration.xml
3. Install Office:
  -->setup.exe /configure configuration.xml
   
### 3. Office Installation Complete
After installation, Office will be ready to use.

💡 Tips:
If you want to install a specific Office version (Office 2016, 2019, etc.), modify the Product ID and Channel in the XML file accordingly.
Ensure you have a stable internet connection for downloading the Office files.

### ERROR MESSAGE
The error message "The configuration file wasn't specified. Error Code: 0-2025 (0)" when running the Office Deployment Tool (ODT) indicates that you haven't specified a configuration file, which is necessary for the installation process.


### ✅ 1. Create a Configuration File:
To install Office, you need a configuration.xml file with installation settings.

## 🔥 Step 1: Create the XML Configuration File

  1. Open Notepad.
  2. Paste the following content for Office 2021 (you can modify it for other versions):
            <Configuration>
              <Add OfficeClientEdition="64" Channel="PerpetualVL2021">
                <Product ID="ProPlus2021Volume">
                  <Language ID="en-us" />
                </Product>
              </Add>
              <Display Level="Full" AcceptEULA="TRUE" />
              <Property Name="AUTOACTIVATE" Value="1" />
            </Configuration>

✅ Explanation:
OfficeClientEdition="64" → For 64-bit Office installation. Use 32 for 32-bit.
Channel="PerpetualVL2021" → Specifies the Office 2021 volume license version.
Language ID="en-us" → Language set to English (US).
  
3. Save the file as:
            configuration.xml
Choose Save as type → All Files.
Save it in the same folder as the Office Deployment Tool.

## 🛠️ Step 2: Install Office with the Configuration File

1. Open Command Prompt as Administrator.
2. Navigate to the folder containing the Office Deployment Tool and configuration.xml:
            cd C:\Path\To\Office\Deployment\Tool
3. First, download the Office installation files:
            setup.exe /download configuration.xml
4. Once the download is complete, install Office:
            setup.exe /configure configuration.xml
