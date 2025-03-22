zelo-cspm/
├── .github/
│   ├── ISSUE_TEMPLATE.md         # Template for reporting issues
│   └── PULL_REQUEST_TEMPLATE.md  # Template for pull requests
├── docs/
│   ├── architecture.md           # Overview of system architecture
│   ├── roadmap.md                # Future milestones and planned features
│   └── installation.md           # Instructions for setup and deployment
├── rules/
│   ├── aws/
│   │   ├── s3.json               # Rule for S3 bucket policies
│   │   ├── ec2.json              # Rule for EC2 misconfigurations
│   │   └── security-groups.json  # Rule for security group settings
│   ├── azure/
│   │   └── sample-rule.json      # Placeholder for Azure-specific rules
│   ├── gcp/
│   │   └── sample-rule.json      # Placeholder for GCP-specific rules
│   └── README.md                 # Guidelines on how to add or modify rules
├── src/
│   ├── cli/
│   │   ├── main.py               # Command-line interface entry point
│   │   └── __init__.py
│   ├── core/
│   │   ├── scan.py               # Scanning logic for cloud resources
│   │   ├── rules_engine.py       # Engine to evaluate rules against resources
│   │   └── __init__.py
│   └── providers/
│       ├── aws.py                # AWS-specific resource fetching
│       ├── azure.py              # Azure-specific resource fetching
│       ├── gcp.py                # GCP-specific resource fetching
│       └── __init__.py
├── tests/
│   ├── test_scan.py              # Unit tests for scanning functionality
│   └── test_rules_engine.py      # Unit tests for rule evaluation logic
├── .gitignore                    # Files and directories to ignore
├── LICENSE                       # Open source license (e.g., Apache 2.0, MIT)
├── README.md                     # Project overview and getting started guide
└── setup.py                      # Setup file for packaging and installation
