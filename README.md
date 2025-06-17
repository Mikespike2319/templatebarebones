# TMH Device Inventory Report Generator

A self-contained, offline HTML tool for generating comprehensive device inventory reports from Microsoft Intune exports. Designed for monthly executive reporting with professional formatting and critical insights.

## Features

- **Fully Offline**: Works without internet connection after initial load
- **Excel Processing**: Parses Intune OData feed exports (.xlsx, .xlsm)
- **Multi-Sheet Support**: Choose from multiple Excel sheets when available
- **Flexible Column Recognition**: Automatically detects and works with available data columns
- **Comprehensive Analytics**:
  - Total device counts by operating system (iOS, Android, Windows)
  - Operating system breakdown with percentages
  - Device model inventory with manufacturer details
  - Compliance status analysis by OS
  - Security status monitoring (encryption)
  - Device activity tracking (last check-in)
- **Executive-Focused Reporting**:
  - Critical issues highlighted as "Urgent Items"
  - Professional summary cards
  - Visual compliance indicators
  - Detailed data tables for analysis
- **Adaptive Interface**: Shows only relevant sections based on available data
- **Print-Ready**: Optimized for A4 paper size and professional presentation

## Usage Instructions

1. **Open the Report Generator**
   - Open `report-generator.html` in any modern web browser (Chrome, Edge, Firefox recommended)

2. **Upload Excel File**
   - Click "Choose Excel File"
   - Select your Intune export (.xlsx or .xlsm file)
   - If multiple sheets exist, choose the desired sheet from the dropdown
   - The report will generate automatically

3. **View Report**
   - **Summary Cards**: Key device counts and totals
   - **Compliance Status**: Visual bars showing compliance by OS
   - **Operating System Breakdown**: Detailed count and percentage by OS
   - **Device Models**: Comprehensive model inventory with manufacturer info
   - **Urgent Items**: Critical issues requiring immediate attention

## Supported Data Columns

The tool automatically recognizes and works with any combination of the following data columns. **All columns are optional** - the tool adapts based on what's available:

### Core Device Information
- **Device ID**: `deviceId`, `device_id`, `Device ID`
- **Device Name**: `deviceName`, `device_name`, `Device name`
- **Operating System**: `operatingSystem`, `os`, `operating_system`, `platform`
- **Model**: `model`, `deviceModel`, `Model`
- **Manufacturer**: `manufacturer`, `make`, `brand`

### Management & Compliance
- **Managed By**: `managedBy`, `managed_by`, `Managed by`
- **Ownership**: `ownership`, `ownershipType`, `Ownership`
- **Compliance**: `complianceStateKey`, `compliance`, `Compliance`
- **Category**: `deviceCategoryKey`, `category`, `Category`

### Status & Activity
- **Last Check-in**: `lastSyncDateTime`, `Last check-in`, `lastcheckin`
- **OS Version**: `osVersion`, `OS version`, `version`
- **Encryption State**: `encryptionState`, `encryption_state`, `encryption`

### Additional Fields
- **Device Key**: `deviceKey`, `device_key`, `key`
- **Deleted Status**: `isDeleted`, `deleted`, `is_deleted`

## Flexible Design

- **No Required Columns**: Works with any Excel file containing device data
- **Automatic Adaptation**: Report sections appear/hide based on available data
- **Column Name Variations**: Recognizes multiple naming conventions (camelCase, snake_case, Title Case)
- **Partial Data Support**: Provides useful insights even with incomplete data sets
- **Multi-Format Support**: Handles various Excel export formats from different systems

## Report Sections

The tool generates the following sections (when relevant data is available):

1. **Summary Cards**: Device counts by OS and totals
2. **Compliance Status**: Visual compliance indicators by operating system
3. **Operating System Breakdown**: Detailed OS distribution with percentages
4. **Device Models**: Comprehensive model inventory sorted by count
5. **Urgent Items**: Critical issues requiring immediate attention:
   - Non-compliant devices
   - Unencrypted devices
   - Inactive devices (not synced in 30+ days)

## Browser Compatibility

- Chrome 60+
- Edge 79+
- Firefox 60+
- Safari 12+

## Version History

- **v2.0 (Current)**
  - Multi-sheet Excel support with sheet selection
  - Operating system breakdown table with percentages
  - Device models inventory with manufacturer details
  - Expanded column mapping for maximum compatibility
  - All columns now optional - adaptive report generation
  - Enhanced executive reporting format
  - Windows device support added
  - Improved error handling and user feedback

- **v1.1**
  - Added flexible column mapping
  - Improved error handling
  - Enhanced UI/UX
  - Added urgent items section

- **v1.0**
  - Initial release
  - Core features implemented

## Technical Notes

- **Self-Contained**: All dependencies included, no external API calls
- **Client-Side Processing**: All data processing happens in the browser
- **Privacy-Focused**: No data leaves your device
- **Lightweight**: Single HTML file with embedded CSS and JavaScript
- **Cross-Platform**: Works on Windows, macOS, and Linux

## Support

For issues or questions, please contact the TMH IT Asset Management team. 