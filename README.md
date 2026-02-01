# Intune-compliance-dashboard
Automated OS Compliance &amp; App Protection Enforcement for Microsoft Intune.
Project Overview

Intune Compliance Maintainer is an automation solution designed to keep Microsoft Intune Compliance Policies and App Protection Policies continuously aligned with the latest supported operating system versions across major platforms.

The solution reduces manual policy updates, improves security posture, and ensures Zero Trust access enforcement by automatically restricting access for devices running outdated or unsupported OS versions.

This project reflects real-world enterprise Intune operations, security automation practices, and cloud identity governance.

🎯 Problem Statement

In large enterprise environments:

OS versions change frequently

Compliance policies become outdated

Manual updates are error-prone and slow

Outdated devices introduce security risk

This project automates the entire lifecycle of OS version enforcement using trusted public data sources and Microsoft Graph.

🚀 Key Features
🌐 Multi-Platform Support

Windows

macOS


🛡 Policy Automation

Updates Intune Compliance Policies

Updates Intune App Protection Policies

Supports minimum OS versions and build ranges


🔄 Smart Update Cadence

Configurable delay between OS release and enforcement

Prevents breaking production devices

Optional force-apply for emergency security enforcement

🔐 Secure Authentication Options

Azure Automation Managed Identity

App Registration with Certificate

App Registration with Secret (Key Vault supported)

🧠 Safety & Reliability

Dry-run mode (preview changes safely)

Downgrade protection

Built-in retry logic

Detailed execution logs

🧩 Architecture & Data Sources

Microsoft Graph API

Intune Compliance Policies

App Protection Policies

Windows Update Catalog

endoflife.date API

Trusted OS lifecycle data

Azure Automation

Secure, scheduled execution using Managed Identity

🛠 Technology Stack

PowerShell 5.1+

Microsoft Graph API

Azure Automation

Azure Key Vault

REST APIs

Enterprise Logging & Error Handling

⚙️ How It Works (High Level)
For iOS, iPadOS, Android, macOS

Fetch latest supported OS version

Apply configurable cadence delay

Update Intune policies once effective

Enforce access restrictions automatically

For Windows

Query Windows Update Catalog via Graph

Identify latest cumulative update builds

Update compliance using:

OS build ranges (recommended)

or minimum OS version

Align app protection policies with selected build


🧪 Execution Modes

Dry Run – Preview changes without modifying policies

🙌 Acknowledgment

Special thanks to the NXTeam Cloud Community for continuous knowledge sharing, collaboration, and technical support throughout my cloud and security learning journey.

📊 Sample Output

| Platform | Policy Type | Current    | Target     | Action       |
| -------- | ----------- | ---------- | ---------- | ------------ |
| iOS      | Compliance  | 17.6.1     | 18.2.1     | Would Update |
| Windows  | Compliance  | 26100.2314 | 26100.2605 | Updated      |
