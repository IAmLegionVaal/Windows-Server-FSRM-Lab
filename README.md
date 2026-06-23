# Windows Server FSRM Lab

![Status](https://img.shields.io/badge/Project-Completed-success)
![Windows Server](https://img.shields.io/badge/Platform-Windows%20Server-0078D4)
![FSRM](https://img.shields.io/badge/Service-FSRM-2F6FED)

A completed Windows Server File Server Resource Manager lab in which I configured storage quotas, file screening, thresholds and reporting for controlled file-server usage.

> **Status:** Completed and validated. This repository documents work already performed in a private lab. Real paths, users, server names and notification details have been generalized.

## Objectives completed

- Installed File Server Resource Manager
- Created quota templates and applied folder quotas
- Configured warning and limit thresholds
- Created file-group and file-screening rules
- Tested blocked and permitted file types
- Generated storage reports
- Reviewed FSRM events and enforcement behavior
- Documented operational findings

## Implementation summary

1. Installed the FSRM role service and management console.
2. Created a test folder structure for controlled storage.
3. Defined quota thresholds and applied a quota template.
4. Configured warning actions before the storage limit was reached.
5. Created file groups for selected extensions.
6. Applied active file screens to restricted folders.
7. Tested both allowed and blocked file operations.
8. Generated reports to review file types and storage usage.
9. Reviewed events and adjusted scope where required.

## Validation commands

```powershell
Get-FsrmQuota
Get-FsrmQuotaTemplate
Get-FsrmFileScreen
Get-FsrmFileGroup
Get-FsrmStorageReport
```

## Outcome

The server enforced the configured storage limits and file-screening rules on the targeted folders. Warning thresholds provided visibility before hard limits were reached, while storage reports supported capacity and policy review.

## Findings

- Quotas controlled storage consumption but did not replace NTFS permissions; both controls served different purposes.
- Template-based configuration made policies easier to apply consistently across multiple folders.
- Active file screening blocked matching files, while passive screening was more suitable for monitoring without enforcement.
- File screening depended on extensions and could not guarantee inspection of a file's true contents.
- Threshold notifications were most useful before users reached the hard limit, allowing corrective action before work was interrupted.
- Reports exposed storage patterns that were not obvious from folder size alone, especially large or duplicate file categories.

## Skills demonstrated

- Windows Server storage administration
- FSRM quotas and templates
- File screening and file groups
- Threshold configuration
- Storage reporting
- Policy validation and troubleshooting
- Capacity-management concepts
- Technical documentation

## Security notes

- No production file paths or user information are included.
- All examples use generalized values.
- The lab was completed in a controlled non-production environment.

## Author

**Dewald Pretorius** — L2 IT Support Engineer
