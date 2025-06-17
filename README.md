# TMH Device Inventory Report Generator

A self-contained, offline HTML tool for generating device inventory reports from Microsoft Intune exports.

## Features

- **Fully Offline**: Works without internet connection after initial load
- **Excel Processing**: Parses Intune OData feed exports (.xlsx)
- **Automatic Calculations**:
  - Total device counts (iOS, Android, Combined)
  - BackStock device count
  - Compliance breakdown
  - Monthly trends
  - Device category counts
  - iOS lifecycle status
- **Export Options**:
  - PDF export
  - HTML export
- **Print-Ready**: Optimized for A4 paper size

## Usage Instructions

1. **Open the Report Generator**
   - Extract `report-generator.html` from the zip file
   - Open in any modern web browser (Chrome, Edge, Firefox recommended)

2. **Upload Excel File**
   - Click "Choose Excel File"
   - Select your Intune export (.xlsx file)
   - The report will generate automatically

3. **View Report**
   - Summary cards show key metrics
   - Compliance bars display status by OS
   - Tables show detailed breakdowns
   - iOS lifecycle status includes EOL information

4. **Export Options**
   - Click "Export to PDF" for a PDF version
   - Click "Export to HTML" for an HTML version
   - Use browser's print function (Ctrl+P/Cmd+P) for direct printing

## Excel File Requirements

The tool expects an Excel file exported from Microsoft Intune with the following columns:
- operatingSystem
- model
- deviceCategoryDisplayName
- complianceState
- lastSyncDateTime

## Browser Compatibility

- Chrome 60+
- Edge 79+
- Firefox 60+
- Safari 12+

## Version History

- v1.0 (Current)
  - Initial release
  - Full TMH branding
  - All core features implemented

## Support

For issues or questions, please contact the TMH IT Asset Management team. 