# Zelo CSPM Architecture

## Overview

**Zelo CSPM** is an open source Cloud Security Posture Management tool designed to detect and remediate misconfigurations in cloud environments. It leverages a modular, extensible architecture that combines a robust scanning engine, a flexible rules engine, and cloud provider integrations. The architecture supports a dual model, where the core (free and open source) functionality is available to all users, while advanced features are offered as paid upgrades.

## Key Components

### 1. CLI Interface
- **Purpose:** Provides a command-line interface (CLI) for users to initiate scans, view results, and manage configurations.
- **Implementation:** Built in Python and serves as the entry point to the system.
- **Integration:** Easily incorporated into CI/CD pipelines for automated scanning during build processes.

### 2. Core Scanning Engine
- **Purpose:** Orchestrates the scanning process across cloud resources.
- **Responsibilities:**
  - Invokes cloud provider modules to fetch resource data.
  - Aggregates and normalizes data for analysis.
  - Passes resource data to the rules engine.
- **Design:** Lightweight and modular to allow scalability and quick integration.

### 3. Rules Engine
- **Purpose:** Evaluates cloud resources against predefined security rules and policies.
- **Components:**
  - **Rule Loader:** Reads JSON/YAML rule files from the `rules/` directory.
  - **Evaluator:** Processes and compares resource data against these rules.
- **Extensibility:** Designed to allow community contributions for new rules and compliance benchmarks.

### 4. Cloud Provider Modules
- **Purpose:** Interface with specific cloud provider APIs (e.g., AWS, Azure, GCP) to retrieve configuration data.
- **Structure:** Separate modules for each provider, enabling independent updates and enhancements.
- **Features:** 
  - Support for agentless scanning.
  - Optionally, integration with agent-based scanning for deeper runtime data.

### 5. Reporting & Remediation
- **Purpose:** Presents scan results and enables remediation actions.
- **Components:**
  - **UI/CLI Reporting:** Outputs results via a minimal UI or CLI.
  - **Automated Remediation Hooks:** (Advanced) Optionally triggers actions to remediate misconfigurations, such as reverting to secure baselines or isolating compromised resources.

### 6. Integration & CI/CD Plugin
- **Purpose:** Enables seamless integration into existing development pipelines.
- **Features:** 
  - A free CI/CD plugin that can trigger scans on each commit or pull request.
  - Enhanced dashboards and gating available in paid tiers.

## Data Flow

1. **User Initiation:** A user triggers a scan via the CLI or CI/CD pipeline.
2. **Resource Retrieval:** The core scanning engine calls the appropriate cloud provider module to retrieve current resource configurations.
3. **Rule Evaluation:** The resource data is passed to the rules engine, which evaluates each resource against community-driven rules.
4. **Results & Reporting:** Findings are aggregated and presented as a report in the UI/CLI output.
5. **Remediation (Optional):** If enabled, automated remediation workflows can trigger actions to address identified issues.

## Deployment Architecture

- **On-Premises / Self-Hosted:** Zelo CSPM can be deployed on local servers or in containerized environments (e.g., Docker, Kubernetes).
- **Cloud-Integrated:** Designed to connect securely with cloud provider APIs using standard authentication methods (e.g., AWS IAM roles, Azure Service Principals).

## Future Enhancements

- **Multi-Cloud Expansion:** Enhance support for additional cloud providers and services.
- **Real-Time Threat Detection:** Integrate advanced analytics and AI to detect anomalies in real-time.
- **Self-Healing Infrastructure:** Implement automated remediation workflows to further reduce risk.
- **Expanded Integrations:** Develop more plugins and integrations with third-party tools like SIEMs, SOAR platforms, and alerting systems.
- **Enhanced UI/UX:** Build a comprehensive web-based dashboard for deep-dive analytics and reporting.

## Conclusion

The modular and extensible architecture of **Zelo CSPM** not only enables rapid adoption and community contributions but also provides a clear path for scaling up to enterprise-grade functionality. This approach ensures that as the threat landscape evolves, the platform can adapt quickly through both internal enhancements and community-driven innovation.

---

*For further details, refer to our [roadmap.md](./docs/roadmap.md) or join our community discussions on GitHub.*
