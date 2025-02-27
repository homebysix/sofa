# SOFA


![Sofa logo](./images/custom_logo.png "Optional title")


Hello 👋,

**SOFA** supports MacAdmins by efficiently tracking and surfacing information on updates for macOS and iOS. It consists of a machine-readable feed and user-friendly web interface, providing continously up-to-date information on XProtect data, OS updates, and the details bundled in those releases.

Updated automatically via GitHub Actions, the SOFA feed is a dynamic, centralized, and accessible source of truth. It can be self-hosted, giving you complete assurances as to the provenance of the data your fleet and coworkers can consume. The goal is to streamline the monitoring of Apple's software releases, thereby boosting security awareness and administrative efficiency.

## Key Features

### Machine-Readable Feed and Web UI
- **JSON Feed**: Provides detailed, machine-readable data optimized for automated tools and scripts
- **Web Interface**: Divided between the major version tabs at the top and organized into sections that cover the latest OS information, XProtect updates, and security details for each OS, SOFA facilitates both quick summaries and deep dives into relevant data points

### Use Cases
SOFA supports a wide array of practical applications, wether for MacAdmin tooling directly or discussing the state of security on Apple platforms with security personnel
- **Xprotect Monitoring**: Keep track of the latest XProtect updates centrally so agents running on your fleet can verify compliance with CIS/mSCP standards, ensuring Apple's tooling is up-to-date
- **Security Overviews**: Surface information on vulnerabilities (CVEs) and their exploitation status (KEV).
- **Track Countdowns**: Know both a timestamp and the days since a release was posted so you can track when management that delays the update being visible will elapse, or just use it to remind users that the clock is ticking on an update that addresses 'critical' issues 
- **Documentation Access**: Use links to quickly view relevant Apple documentation and check detailed CVE information CVE.org, CISA.gov and NVD, and correlate those CVE's across platforms or major versions
- **Download Universal Mac Assistant**: Access the latest and all 'active' (currently signed) IPSW/Universal Mac Assistant (UMA) download links. These can be integrated into your custom reprovisioning workflows, such as EraseAndInstall, to streamline and enhance your device re-purpose/deployment processes
- **Self-Hosting**: Take control of the SOFA feed by self-hosting. Establish your fork as the authoritative source in your environment. Tailor the feed to meet your specific needs and maintain complete autonomy over its data

## Web UI Overview

### OS Version Card
- **Latest OS Version:** View details for the latest macOS and iOS releases, including version numbers, build identifiers, and release dates
- **Download Links:** Direct access to download latest installers like IPSW files (coming soon!) or Universal Mac Assistant (UMA) packages
- **Security and Documentation Links:** Quick access to relevant Apple documentation and security advisories

### XProtect Data Card (macOS Only)
- **Latest Versions Information:** Track the most current versions of XProtect
- **Verification Baseline:** Use as a baseline info for use in custom tools to ensure XProtect is up-to-date across your macOS fleet. This could be running compliance scripts or extension attributes. See some starter examples in [Tools](./tool-scripts)
- **Update Frequency Details:** See when XProtect was updated and the days since the latest release

### Security Updates Listing
- **Release Timelines:** Overview of the release dates and intervals between the latest security updates.
- **Vulnerability Details:**  For each CVE, links are provided to view detailed records at CISA.gov or CVE.org. Use 'Command-click' to open a CVE record on the NVD website, highlighting detailed info on actively exploited vulnerabilities and related security advisories
- **Search and Highlight**: Search for specific CVEs to identify which OS updates address the vulnerabilities

## Getting Started

### Access the Web UI
Visit the [SOFA Web UI](https://macadmins.github.io/sofa/) to start exploring SOFA's features

### Use the Feed Data
Access the feed directly for integration with automated tools or scripts. For production use, we strongly recommend self-hosting the feed to enhance reliability and security. For guidance on how to utilize and implement the feed, explore examples in the [Tools](./tool-scripts) section. For details on self-hosting, please refer to the section below.


### Self-Hosting SOFA

We believe that organizations needing tight control and ownership of the data they rely on should consider self-hosting SOFA. By cloning the repository into your own GitHub account and activating GitHub Actions to automatically build the feed at set intervals — or implementing a similar setup on platforms like GitLab — you ensure full control over how the data is determined, updated, and utilized. Additional documentation on self-hosting will be available to guide you through this process.