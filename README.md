# TMH Device Inventory Report Generator

A self-contained, offline HTML tool for generating comprehensive device inventory reports from Microsoft Intune exports. Designed for monthly executive reporting with professional formatting and critical insights.

## Features

- **Fully Offline**: Works without internet connection after initial load
- **File Processing**: Parses Intune OData feed exports (.xlsx, .xlsm, .csv)
- **Multi-Sheet Support**: Choose from multiple Excel sheets when available
- **Flexible Column Recognition**: Automatically detects and works with available data columns
- **Comprehensive Analytics**:
  - Total device counts by operating system (iOS, Android, Windows)
  - Operating system breakdown with percentages
  - Device model inventory with manufacturer details
  - Compliance status analysis by OS
  - Security status monitoring (encryption)
  - Device activity tracking (last check-in)
- **iOS Lifecycle Management**:
  - End-of-life (EOL) tracking for iOS devices
  - Device lifecycle status indicators (Good, Warning, Critical)
  - Hardcoded iOS device EOL database for accurate reporting
- **Executive-Focused Reporting**:
  - Critical issues highlighted as "Urgent Items"
  - Professional summary cards
  - Visual compliance indicators
  - Detailed data tables for analysis
- **Device Model Windows**: Separate detailed views for iOS and Android device inventories
- **Export Capabilities**: 
  - PDF export for professional reporting
  - Print-optimized layouts
- **Adaptive Interface**: Shows only relevant sections based on available data
- **Print-Ready**: Optimized for A4 paper size and professional presentation

## Usage Instructions

1. **Open the Report Generator**
   - Open `report-generator.html` in any modern web browser (Chrome, Edge, Firefox recommended)

2. **Upload File**
   - Click "Choose Excel or CSV File"
   - Select your Intune export (.xlsx, .xlsm, or .csv file)
   - If uploading Excel with multiple sheets, choose the desired sheet from the dropdown
   - The report will generate automatically

3. **View Report**
   - **Summary Cards**: Key device counts and totals
   - **Compliance Status**: Visual bars showing compliance by OS
   - **Operating System Breakdown**: Detailed count and percentage by OS
   - **Device Models**: Comprehensive model inventory with manufacturer info
   - **iOS Lifecycle**: End-of-life tracking and status for iOS devices
   - **Urgent Items**: Critical issues requiring immediate attention

4. **Export Options**
   - **PDF Export**: Click "Export to PDF" for professional single-page reports
   - **iOS Models**: Click "iOS Models" to view detailed iOS device inventory in separate window
   - **Android Models**: Click "Android Models" to view detailed Android device inventory in separate window

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
- **Multi-Format Support**: Handles Excel (.xlsx, .xlsm) and CSV (.csv) export formats from different systems

## Report Sections

The tool generates the following sections (when relevant data is available):

1. **Summary Cards**: Device counts by OS and totals
2. **Compliance Status**: Visual compliance indicators by operating system
3. **Operating System Breakdown**: Detailed OS distribution with percentages
4. **Device Models**: Comprehensive model inventory sorted by count
5. **iOS Device Lifecycle**: End-of-life tracking with status indicators:
   - **Good**: Device supported with current iOS versions
   - **Warning**: Device approaching end-of-life
   - **Critical**: Device past end-of-life, security risk
6. **Urgent Items**: Critical issues requiring immediate attention:
   - Non-compliant devices
   - Unencrypted devices
   - Inactive devices (not synced in 30+ days)

## Export Features

### PDF Export
- Single-page professional reports optimized for A4 paper
- Maintains TMH branding and formatting
- Suitable for executive presentations and archival

### Device Model Windows
- **iOS Models Window**: Dedicated view showing all iOS devices with:
  - Device names and models
  - Compliance status
  - End-of-life information
  - Manufacturer details
- **Android Models Window**: Dedicated view showing all Android devices with detailed specifications

## iOS Lifecycle Database

The tool includes a comprehensive hardcoded database of iOS device end-of-life dates for accurate lifecycle tracking:
- iPhone models from iPhone 5s through iPhone 15 series
- iPad models including Air, mini, and Pro variants
- iPod touch models
- Automatic status calculation based on current date vs. EOL date

## Browser Compatibility

- Chrome 60+
- Edge 79+
- Firefox 60+
- Safari 12+

## Version History

- **v2.1 (Current)**
  - PDF export functionality with single-page optimization
  - iOS lifecycle management with EOL tracking
  - Separate iOS and Android device model windows
  - Enhanced device status indicators
  - Improved executive reporting format

- **v2.0**
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