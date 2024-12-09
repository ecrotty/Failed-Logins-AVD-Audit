# AVD Connection Health Monitoring Workbook

A comprehensive Azure Workbook for monitoring Azure Virtual Desktop (AVD) connection health, focusing on connection failures and host performance metrics. This workbook provides real-time insights into your AVD environment's health status and helps identify potential issues before they impact users.

## Features

- **Connection Status Monitoring**: Detailed tracking of all connection attempts and their outcomes
- **Host Health Analysis**: Failure rate analysis and health scoring for each session host
- **Success Trend Visualization**: Time-based visualization of successful connections
- **Performance Metrics**: Comprehensive host performance indicators
- **Alert-Ready Metrics**: Pre-configured thresholds for common issues:
  - Host failure rates above 50%
  - Hosts with health scores below 70%
  - Repeated connection failures within 1 hour

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

The workbook is divided into several sections:

1. **Connection Status Detail**: Shows all connection attempts and their outcomes
2. **Host Health Analysis**: Displays failure rates for each session host
3. **Successful Connection Trend**: Shows the pattern of successful connections over time
4. **Host Health Status**: Provides a comprehensive health score for each session host

Each section includes:
- Detailed metrics and visualizations
- Alert considerations
- Performance indicators

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
