# VMware-PowerCLI-Use-Cases
Automation scripts for managing and optimizing VMware environments using PowerCLI.

VMware Automation Toolkit (PowerCLI) - README
============================================

Contents:
- Credentials/_Credential_Manager.ps1  : Run this once to store vCenter IP and credentials securely.
- Scripts/01_VM_Inventory.ps1          : VM inventory report
- Scripts/02_VM_Performance.ps1        : VM performance summary
- Scripts/03_Snapshot_Report.ps1       : Snapshot report and cleanup
- Scripts/04_VM_Power_Operations.ps1   : VM power operations (Start/Stop/Restart)
- Scripts/05_Datastore_Usage.ps1       : Datastore usage report
- Scripts/06_Host_Health.ps1           : Host health and resource report
- Scripts/07_Network_Config.ps1        : Network configuration summary
- Scripts/08_Orphaned_VMs.ps1          : Orphaned VM detection (placeholder)
- Scripts/09_VMTools_Audit.ps1         : VM Tools status audit
- Scripts/10_VM_Compliance_Check.ps1   : VM naming and tagging compliance

Usage:
1. Copy the 'VMwareReports' folder to C:\ (or keep the path and update scripts accordingly).
2. Run C:\VMwareReports\Credentials\_Credential_Manager.ps1 to store credentials (first time only).
3. Run any script from the Scripts folder. They will auto-load credentials and connect to vCenter.
4. Reports will be saved to C:\VMwareReports\Reports and logs to C:\VMwareReports\Logs\execution_log.txt

Security:
- Credentials are stored using Export-Clixml which uses DPAPI to protect credentials to the current user.
- Do NOT copy the vc_credentials.xml file to another machine or user.

Notes:
- Customize thresholds and VM lists in each script as required by your environment.
- The orphaned VM detection script contains a placeholder region — please adapt to your datastore browsing needs.
