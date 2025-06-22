# SD-WAN Orchestration Project

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Testing](#testing)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview

This project focuses on the orchestration and management of an SD-WAN infrastructure using Cisco Viptela vManage. The primary goal is to configure and manage devices across multiple sites with centralized templates and policies, ensuring secure and efficient communication. This README provides detailed instructions on setting up, configuring, and testing the SD-WAN environment.

## Features

- Centralized configuration management via vManage.
- Template-based device configurations for consistency.
- Policy enforcement using Access Control Lists (ACLs) and other security measures.
- Comprehensive testing procedures to validate network functionality.
- Detailed documentation and visual aids for each step.

## Prerequisites

Before you begin, ensure you have the following:

- **Software**: EVE-NG, Cisco Viptela vManage, vBond, vSmart, vEdge images.
- **Tools**: WinSCP, PuTTY, or any SSH client for secure file transfer and CLI access.
- **Network Setup**: Basic understanding of SD-WAN architecture and routing protocols like BGP and OSPF.

## Installation

1. **Clone the Repository**:
    ```bash
    git clone git@github.com:HAC5R00T/SD-WAN.git 
    cd sdwan-orchestration
    ```

2. **Setup EVE-NG Environment**:
    - Import necessary VM images into EVE-NG.
    - Configure network topology as per the project requirements.

3. **Initial Device Configuration**:
    - Set up basic configurations for vManage, vBond, vSmart, and vEdge devices.
    - Ensure all devices are reachable and can communicate within the network.

## Configuration

### Centralized Configuration with Templates

- **Feature Templates**:
    - Define feature templates for various components such as interfaces, VPNs, BGP, and OSPF.
    - Apply these templates to ensure consistent and scalable configurations across all devices.

- **Policy Templates**:
    - Create and apply policy templates for traffic management and enhanced security.
    - Examples include INGRESS and EGRESS ACL policies.

### Device-Specific Configurations

- **Transport and Management VPN**:
    - Configure VPN 0 for transport interfaces.
    - Configure VPN 512 for management purposes.

- **Service VPNs**:
    - Service VPN 10: Data traffic management.
    - Service VPN 20: Voice traffic management.
    - Service VPN 1: User LAN management.

### Routing Protocols

- **BGP**:
    - Configure BGP for Internet-side routing within VPN 0.
- **OSPF**:
    - Configure OSPF for MPLS-side routing and VRF exchange.

## Usage

1. **Access vManage Dashboard**:
    - Log in to the vManage web interface to monitor and manage the SD-WAN fabric.
    - Apply configured templates and policies.

2. **Device Attachment**:
    - Select and attach devices from the available list to apply configured policies and templates.

3. **Validation and Deployment**:
    - Validate configurations before deployment.
    - Push configurations to respective devices and ensure successful application.

## Testing

### Connectivity Tests

- **Ping Tests**:
    - Perform ping tests across different VPNs to verify connectivity.
    - Example: Ping tests for Site 400 (VPN 10).

- **Traceroute Tests**:
    - Use traceroute to map the path of data packets and identify potential bottlenecks.

### DHCP and VRRP Tests

- Verify DHCP functionality by ensuring devices obtain IP addresses correctly.
- Test VRRP configurations for gateway redundancy.

## Results

- Successful onboarding and communication of all controllers (vBond, vSmart, vManage).
- Validated secure and efficient network operations through comprehensive testing.
- Effective policy enforcement and traffic management.

## Contributing

We welcome contributions from the community! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeatureName`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeatureName`).
5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any questions or further information, please contact:

- **Name**: Mohamed Aziz Akrout
- **Email**: mohamedazizakrout@gmail.com
- **GitHub**:(https://github.com/HAC5R00T) 

---

Thank you for your interest in the SD-WAN Orchestration project!
