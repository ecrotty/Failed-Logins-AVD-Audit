# AVD Connection Health Monitoring Workbook

A comprehensive Azure Workbook for monitoring Azure Virtual Desktop (AVD) connection health, analyzing the complete connection lifecycle across user experience, connection timing, and host health. This workbook provides real-time insights into your AVD environment's health status and helps identify potential issues before they impact users.

## Features

### 1. 🏥 User Health Status
- User connection success rates monitoring
- Recent failures and connection patterns tracking
- Health scores based on connection reliability
- User-specific connection analysis

### 2. ⏱️ Connection Timing Analysis
- Connection duration pattern analysis
- Identification of potential hanging sessions
- Connection state transition tracking
- Performance thresholds:
  - Warning: > 30 seconds
  - Critical: > 60 seconds
  - Severe: > 120 seconds

### 3. 📊 Host Health Analysis
- Complete connection lifecycle tracking (Started → Connected → Completed)
- Failed connection identification (sessions that start but never connect)
- Success rate calculations based on actual connection attempts
- Health status thresholds:
  - Excellent: ≥90% success rate
  - Good: 70-89% success rate
  - Needs Attention: 50-69% success rate
  - Critical: <50% success rate

### 4. 👥 End-User Experience Analysis
- Connection patterns and success rates per user
- Client type performance analysis
- User-specific health scoring
- Recent user activity monitoring

## Prerequisites

- An Azure subscription
- A Log Analytics workspace
- Azure Virtual Desktop deployment
- Proper permissions to access Azure Monitor and Log Analytics

## Installation

1. Download the `failed-logins-avd-generic.json` file
2. Navigate to Azure Portal > Azure Monitor > Workbooks
3. Click "New" to create a new workbook
4. Click the Advanced Editor button (</>) 
5. Replace the existing code with the content from `failed-logins-avd-generic.json`
6. Configure the following parameters in the JSON:
   - Replace `YOUR_SUBSCRIPTION_ID` with your Azure subscription ID
   - Replace `YOUR_RESOURCE_GROUP` with your resource group name
   - Replace `YOUR_WORKSPACE_NAME` with your Log Analytics workspace name

## Usage

The workbook is divided into several key sections:

1. **Connection Status Detail**
   - All connection attempts and outcomes
   - Authentication issue highlighting
   - Host health issue tracking

2. **Host Health Analysis**
   - Connection lifecycle analysis
   - Success rate calculations
   - Health status monitoring

3. **Connection Timing Analysis**
   - Duration pattern analysis
   - Hanging session identification
   - State transition tracking

4. **User Health Status**
   - User-specific success rates
   - Recent failure tracking
   - Health score calculations

5. **End-User Experience Analysis**
   - Connection patterns
   - Client type performance
   - User success rates

Each section includes:
- Detailed metrics and visualizations
- Alert considerations
- Performance indicators
- Health status thresholds

## Connection States

The workbook tracks various connection states:
- Started: Initial connection attempt
- Connected: Successfully established connection
- Completed: Normal session termination
- Failed: Started but never reached Connected state

## Customization

The default time window is set to 24 hours. To modify this:
1. Locate the `ago(24h)` parameter in the queries
2. Replace with your desired time window (e.g., `ago(7d)` for 7 days)

## Contributing

Contributions are welcome! Please read our [Contributing Guide](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## License

This project is licensed under the BSD-3-Clause License - see the [LICENSE](LICENSE) file for details.

## Author

Ed Crotty (ecrotty@edcrotty.com)

## Repository

https://github.com/ecrotty/Failed-Logins-AVD-Audit

## Support

For support, please open an issue in the GitHub repository.
