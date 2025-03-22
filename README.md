# Zelo CSPM

**Zelo CSPM** is an open source Cloud Security Posture Management (CSPM) tool designed to help organizations detect and remediate misconfigurations in cloud environments. By combining a community-driven open source engine with advanced paid tiers for multi-cloud and real-time scanning, Zelo CSPM offers a transparent and scalable security solution.

## Key Features

- **Open Source CSPM**: Detect misconfigurations in AWS, Azure, and GCP with a free, open source scanning engine.
- **Vulnerability Management**: Baseline scanning for known CVEs with the option for ML-based prioritization.
- **Compliance Monitoring**: Basic CIS checks are available for free, with advanced reporting for PCI, HIPAA, SOC 2, and more.
- **Flexible Deployment**: Supports both agentless scanning for quick setup and agent-based scanning for continuous monitoring.
- **CI/CD Pipeline Integration & Container Image Scanning**: Seamlessly integrate Zelo CSPM into your development pipelines to scan container images and infrastructure as code, catching vulnerabilities early in the build process.
- **Extensible Rules Engine**: Community-driven rules that can be extended and customized over time.

## Repository Structure

- **.github/**: Issue and pull request templates.
- **docs/**: Documentation including architecture, roadmap, and installation guides.
- **rules/**: JSON rule files for detecting misconfigurations in AWS, Azure, and GCP.
- **src/**: Source code including the command-line interface, core scanning logic, and cloud provider integrations.
- **tests/**: Unit tests for ensuring the reliability of scanning and rules evaluation.
- **LICENSE**: The open source license governing use and distribution.
- **setup.py**: Script for packaging and installation.

## Getting Started

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/YourOrg/zelo-cspm.git
   cd zelo-cspm
