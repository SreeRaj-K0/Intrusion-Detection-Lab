
# Simple Intrusion Detection Lab With pfSense, Snort, Splunk

## Objective

This project aims to demonstrate a practical setup of an intrusion detection lab using pfSense for network management, Snort for intrusion detection, and Splunk for log analysis. The objective is to showcase proficiency in configuring and integrating these tools to monitor and analyze network traffic for potential threats.

## Learning Goals

- Gain hands-on experience in configuring pfSense for network management.
- Implement and customize Snort rules for intrusion detection.
- Set up Splunk for log aggregation, analysis, and visualization of Snort alerts.
- Practice monitoring network traffic and responding to simulated cybersecurity incidents.
- Showcase effective documentation and communication of technical setups and procedures.

## Features

- **Network Configuration**: Setup of LAN and WAN interfaces on pfSense.
- **Intrusion Detection**: Utilization of Snort for real-time threat detection.
- **Log Analysis**: Integration of Splunk for centralized log management and analysis of Snort alerts.
- **Visualization**: Creation of custom dashboards in Splunk for visualizing security incidents.

## Setup Instructions

Follow these steps to replicate the intrusion detection lab environment:

### 1. Setting Up pfSense

1.1. **Download pfSense**:
   - Visit the [pfSense website](https://www.pfsense.org/) and download the latest stable version suitable for your hardware or virtual machine platform.

1.2. **Install pfSense**:
   - Follow the installation guide provided by pfSense to install the operating system on your chosen platform.
   
1.3. **Configure LAN and WAN Interfaces**:
   - Access the pfSense web interface using your web browser (default IP: `192.168.1.1`).
   - Navigate to `Interfaces` > `Assignments` and configure LAN (e.g., `192.168.3.0/24`) and WAN interfaces (e.g., `176.144.134.0/24`) according to your network setup.

1.4. **Install Snort**:
   - Go to `System` > `Package Manager` > `Available Packages`.
   - Search for "Snort" and click `Install` to add Snort to your pfSense installation.

### 2. Configuring Snort

2.1. **Enable Snort on Interfaces**:
   - Navigate to `Services` > `Snort` and configure Snort to monitor selected interfaces (e.g., LAN and WAN).
   - Customize detection and prevention rules based on your security requirements.

2.2. **Configure Snort Alerts**:
   - Define alert settings to log and respond to potential network threats.
   - Verify Snort is actively monitoring and generating alerts for detected incidents.

### 3. Installing and Configuring Splunk

3.1. **Download Splunk**:
   - Visit the [Splunk website](https://www.splunk.com/) and download the latest version of Splunk Enterprise or Splunk Free.

3.2. **Install Splunk**:
   - Follow the installation instructions provided by Splunk to install the software on a dedicated server or virtual machine.

3.3. **Configure Splunk Forwarder**:
   - Optionally, install Splunk Universal Forwarder on pfSense or a separate machine to forward Snort logs to Splunk.
   - Configure inputs.conf on Splunk Forwarder to collect Snort logs from pfSense.

3.4. **Create Splunk Index and Dashboard**:
   - Access the Splunk web interface (default URL: `http://localhost:8000`) and log in.
   - Create an index for Snort logs and configure it to receive and index incoming logs.
   - Design custom dashboards in Splunk to visualize and analyze Snort alerts effectively.

## Usage

Upon completion of setup, use the lab environment to:

- Monitor network traffic and detect potential intrusions in real-time.
- Analyze and investigate Snort alerts to identify security incidents.
- Practice incident response procedures in a controlled environment.

## Contributing

Contributions and feedback are welcome! If you have suggestions for improvements or additional features, please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

## Conclusion

This documentation serves to showcase proficiency in setting up and managing an intrusion detection lab using pfSense, Snort, and Splunk. It demonstrates practical skills in network security monitoring, log analysis, and incident response, making it a valuable resource for cybersecurity professionals and enthusiasts alike.

By documenting this project, I aim to highlight my ability to effectively deploy and manage cybersecurity tools in a practical setting, preparing me for roles that require hands-on experience and technical expertise in intrusion detection and response.
