# Detection Rules for Security Monitoring

This repository contains detection rules designed to enhance security monitoring and threat detection. Authored by **EBLA-KW**, these rules help identify and alert on unusual login activity, potential brute force attacks, and high-risk access attempts. Each rule logs only essential fields to optimize data storage.

---

## Detection Rules Overview

### 1. Failed Login Outside Working Hours
- **Description**: Detects failed login attempts outside of standard business hours to identify possible unauthorized access.
- **Severity**: Medium
- **Frequency**: Run Hourly
- **Logged Fields**: `Account`, `IP Address`, `Login Time`

### 2. Failed VPN Login Investigation with Threat Intelligence
- **Description**: Monitors failed VPN login attempts and cross-references them with known threat intelligence indicators to identify high-risk access attempts.
- **Severity**: High
- **Frequency**: Run Every 30 Minutes
- **Logged Fields**: `Account`, `IP Address`, `VPN Server`, `Time`, `Threat Match`

### 3. Multiple Failed Login Attempts
- **Description**: Flags accounts with multiple failed login attempts in a short period, which may indicate brute force attacks.
- **Severity**: High
- **Frequency**: Run Every 15 Minutes
- **Logged Fields**: `Account`, `IP Address`, `Failure Count`, `Last Attempt Time`

### 4. Successful Login Outside Working Hours
- **Description**: Identifies successful logins occurring outside of working hours to detect unusual user activity.
- **Severity**: Medium
- **Frequency**: Run Hourly
- **Logged Fields**: `Account`, `IP Address`, `Login Time`

---

## Usage and Configuration

1. **Deployment**: Each rule should be deployed to your security monitoring platform, with specified frequencies and severity levels configured.
2. **Minimized Logs**: These rules have been designed to log only essential fields to minimize data usage. Adjustments can be made based on specific requirements.
3. **Review Schedule**: Regularly review the logs generated by these rules to validate their effectiveness and adjust the configurations as necessary.

## Author
These detection rules were created and are maintained by **EBLA-KW**.

## License
This repository is licensed under the MIT License. See `LICENSE` for more details.
