# TMH Device Inventory Report Generator

A self-contained, offline HTML tool for generating device inventory reports from Microsoft Intune exports.

## Features

- **Fully Offline**: Works without internet connection after initial load
- **Excel Processing**: Parses Intune OData feed exports (.xlsx, .xlsm)
- **Automatic Calculations**:
  - Total device counts (iOS, Android, Combined)
  - Compliance status by OS
  - Security status (encryption)
  - Device activity status
- **Urgent Items Highlighting**:
  - Non-compliant devices
  - Unencrypted devices
  - Inactive devices (30+ days)
- **Print-Ready**: Optimized for A4 paper size

## Usage Instructions

1. **Open the Report Generator**
   - Open `report-generator.html` in any modern web browser (Chrome, Edge, Firefox recommended)

2. **Upload Excel File**
   - Click "Choose Excel File"
   - Select your Intune export (.xlsx or .xlsm file)
   - The report will generate automatically

3. **View Report**
   - Summary cards show key metrics
   - Compliance bars display status by OS
   - Urgent items are highlighted for immediate attention

## Excel File Requirements

The tool expects an Excel file exported from Microsoft Intune with the following columns:
- deviceKey
- deviceId
- deviceName
- operatingSystem
- complianceStateKey
- lastSyncDateTime
- encryptionState

The tool is flexible and will recognize common variations of these column names.

## Browser Compatibility

- Chrome 60+
- Edge 79+
- Firefox 60+
- Safari 12+

## Version History

- v1.1 (Current)
  - Added flexible column mapping
  - Improved error handling
  - Enhanced UI/UX
  - Added urgent items section
- v1.0
  - Initial release
  - Core features implemented

## Support

For issues or questions, please contact the TMH IT Asset Management team. 