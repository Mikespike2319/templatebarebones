# TMH Device Inventory Report Generator

A comprehensive, self-contained HTML tool for generating professional device inventory reports from Microsoft Intune exports. Designed for executive presentations with flexible layouts, enhanced device categorization, and critical lifecycle insights.

## ✨ Key Features

### **Professional Reporting**
- **Flexible Layout Modes**: Toggle between Portrait and Landscape layouts for different presentation needs
- **HTML Export**: Clean HTML export for screenshots and presentations (removes interactive elements)
- **Print Optimization**: A4 format with exact color printing and page break controls
- **Executive Styling**: Professional compact card design with clean typography

### **Enhanced Device Management**
- **Comprehensive iOS Lifecycle**: Complete EOL database including iPad 6th/7th gen, iPad Air 2, and iPad Pro models
- **Smart Android Categorization**: Enhanced detection for HC50 Zebra, TC52/TC50 Zebra, MC Series, Rover/Honeywell devices
- **Windows Device Filtering**: Automatic exclusion of Windows devices for mobile-focused reporting
- **ConfigMgr Integration**: Proper handling of "See ConfigMgr" devices in compliance calculations

### **Advanced Analytics**
- **Platform-Separated OS Breakdown**: Clean separation of iOS, Android, and Windows with smart iOS summarization
- **Monthly Trend Tracking**: CFO-style monthly tables with device counts, deltas, and color-coded indicators
- **Adjustable Lifecycle Summary**: Configurable display with sorting, highlighting, and compact modes
- **Urgent Items Management**: Critical device identification with severity levels

### **Data Processing**
- **Fully Offline**: Works without internet connection after initial load
- **Multi-Format Support**: Excel (.xlsx, .xlsm) and CSV files
- **Flexible Column Recognition**: Adapts to available data columns
- **Historical Data**: Persistent monthly tracking with localStorage

## 🚀 Quick Start

1. **Open** `report-generator.html` in any modern web browser
2. **Upload** your Intune export file (.xlsx, .xlsm, or .csv)
3. **Toggle Layout** between Portrait and Landscape modes as needed
4. **Export** as HTML for screenshots or presentations
5. **Track Trends** using the monthly inventory analysis

## 📊 Report Sections

### **Executive Summary Cards**
- iOS, Android, and Total device counts
- Professional gradient styling with hover effects
- Real-time updates based on data

### **Compliance Analysis**
- Visual compliance bars by platform
- Three-category compliance: Compliant, Unknown (ConfigMgr), Non-Compliant
- Percentage calculations excluding ConfigMgr devices

### **Operating System Breakdown**
- **iOS**: Top 3 versions + summary of remaining
- **Android**: All versions displayed individually
- **Windows**: All versions displayed individually
- Platform-separated for clean organization

### **Device Lifecycle Management**
- **iOS Lifecycle**: Complete EOL tracking with status indicators
- **Android Lifecycle**: HC50 Zebra (2029), TC52/TC50 (2028-2030), MC Series (2026-2029)
- **Status Categories**: Good (supported), Warning (approaching EOL), Critical (past EOL)

### **Monthly Trend Analysis**
- CFO-style monthly tables with device counts and deltas
- Color-coded trend indicators (↑ green, ↓ red, → neutral)
- Historical data persistence with automatic monthly progression

### **Urgent Items Dashboard**
- Critical devices requiring immediate attention
- Severity levels: High, Medium, Low
- Smooth scrolling with visual indicators

## 🎛️ Layout Modes

### **Portrait Mode** (Default)
- Optimized for standard screens and presentations
- Single-column layout for focused viewing
- Professional spacing and typography

### **Landscape Mode**
- Wide-screen optimization for executive dashboards
- Multi-column layouts for comprehensive overview
- Enhanced data density for detailed analysis

## 📱 Device Categorization

### **iOS Devices**
- Complete lifecycle database with EOL dates
- iPhone models: iPhone 5s through iPhone 15 series
- iPad models: iPad 6th/7th gen, iPad Air 2, iPad Pro variants
- iPod touch models

### **Android Devices**
- **HC50 Zebra**: Healthcare-focused devices (EOL: 2029)
- **TC52/TC50 Zebra**: Terminal devices (EOL: 2028-2030)
- **MC Series Zebra**: Mobile computers (EOL: 2026-2029)
- **Rover/Honeywell**: Rugged devices (EOL: Variable)
- **Samsung/Google**: Consumer devices (EOL: 2027-2030)
- **Other Android**: Various manufacturers (EOL: Unknown)

### **Windows Devices**
- Automatically filtered out for mobile-focused reporting
- Can be included for comprehensive analysis
- Surface, Dell, HP, Lenovo device detection

## 📈 Monthly Trend Tracking

### **Features**
- Automatic monthly progression
- Historical data persistence
- Trend indicators with color coding
- CFO-style presentation format

### **Data Management**
- Auto-fill current month data
- Export historical data to CSV
- Clear historical data option
- Local storage for data persistence

## 🎨 Export Options

### **HTML Export**
- Clean, presentation-ready HTML
- Removes interactive elements for screenshots
- Maintains professional styling
- Perfect for executive presentations

### **Print Optimization**
- A4 paper size formatting
- Exact color reproduction
- Page break controls
- Professional typography

## 🔧 Configuration Options

### **Lifecycle Summary Settings**
```javascript
const lifecycleConfig = {
    maxModels: 'all',        // 'all' or number
    sortBy: 'count',         // 'count' or 'eol'
    highlightCritical: true, // Highlight critical devices
    compactMode: true        // Compact display
};
```

### **Monthly Analysis Settings**
- Automatic current month detection
- Historical data retention
- Trend calculation algorithms
- Export formatting options

## 📋 Supported Data Columns

The tool automatically recognizes these column variations:

### **Core Device Information**
- Device Name: `deviceName`, `Device name`
- Model: `model`, `Model`
- Operating System: `operatingSystem`, `OS version`
- Manufacturer: `manufacturer`

### **Management & Compliance**
- Managed By: `managedBy`, `Managed by`
- Ownership: `ownership`, `Ownership`
- Compliance: `complianceStateKey`, `Compliance`
- Category: `deviceCategoryKey`, `Category`

### **Status & Activity**
- Last Check-in: `lastSyncDateTime`, `Last check-in`
- OS Version: `osVersion`, `OS version`

## 🏥 Healthcare-Specific Features

### **Device Filtering**
- Automatic Windows device exclusion for mobile focus
- Healthcare device categorization (HC50, TC52/TC50)
- ConfigMgr integration for compliance reporting

### **Compliance Standards**
- Three-tier compliance system
- ConfigMgr device handling
- Unassigned device identification

## 🔄 Version History

### **v3.0 (Current)**
- **Layout Flexibility**: Portrait/Landscape mode toggling
- **HTML Export**: Clean export for presentations
- **Enhanced Device Categorization**: Improved Android detection
- **iPad EOL Database**: Complete iPad lifecycle tracking
- **OS Breakdown Improvements**: Platform separation and iOS summarization
- **Monthly Trend Analysis**: CFO-style tables with persistence
- **ConfigMgr Integration**: Proper compliance calculation
- **Windows Device Filtering**: Mobile-focused reporting

### **v2.1**
- PDF export functionality
- iOS lifecycle management
- Separate device model windows
- Enhanced status indicators

### **v2.0**
- Multi-sheet Excel support
- Operating system breakdown
- Device models inventory
- Expanded column mapping

### **v1.0**
- Initial release with core features

## 🌐 Browser Compatibility

- **Chrome**: 60+
- **Edge**: 79+
- **Firefox**: 60+
- **Safari**: 12+

## 💻 Technical Specifications

- **Self-Contained**: Single HTML file with embedded dependencies
- **Client-Side Processing**: All data processing in browser
- **Privacy-Focused**: No data transmission
- **Cross-Platform**: Windows, macOS, Linux support
- **Lightweight**: Optimized for performance

## 📞 Support

For technical support or feature requests, contact the TMH IT Asset Management team.

---

**Tallahassee Memorial Hospital** - IT Asset Management Report Generator  
*Professional device inventory reporting for healthcare environments* 