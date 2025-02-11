## 7.11.1 (2024-04-19)


### Bug Fixes

* **AZ-1395:** precondition for premium account_tier 608a448


### Continuous Integration

* **AZ-1391:** enable semantic-release [skip ci] 172522f
* **AZ-1391:** update semantic-release config [skip ci] df8c7e1

# v7.11.0 - 2024-03-29

Added
  * [GH-14](https://github.com/claranet/terraform-azurerm-storage-account/issues/14): add `public_network_access_enabled` parameter

# v7.10.0 - 2023-12-22

Added
  * AZ-1317: Add a precondition to disallow PITR on Premium storage accounts

# v7.9.0 - 2023-12-08

Added
  * AZ-1292: Add `cross_tenant_replication_enabled` parameter for enabling cross tenant replication support

# v7.8.0 - 2023-09-01

Breaking
  * AZ-1153: Remove `retention_days` parameters, it must be handled at destination level now. (for reference: [Provider issue](https://github.com/hashicorp/terraform-provider-azurerm/issues/23051))

# v7.7.0 - 2023-05-26

Added
  * [GH-6](https://github.com/claranet/terraform-azurerm-storage-account/issues/6): Expose `last_access_time_enabled` variable within blob data protection

# v7.6.1 - 2023-05-12

Fixed
  * AZ-1079: Fix example

# v7.6.0 - 2023-04-21

Added
  * AZ-1065: Add private_link_access option
  * [GH-4](https://github.com/claranet/terraform-azurerm-storage-account/issues/4): Add an example with multiple storage accounts

Fixed
  * AZ-996: Ensure Premium file shares have a minimum size of 100Gb

# v7.5.0 - 2023-03-03

Added
  * AZ-924: Add support for SFTP

# v7.4.1 - 2023-02-08

Fixed
  * AZ-995: Do not enable large file if account replication is not `LRS` or `ZRS`

# v7.4.0 - 2022-12-23

Fixed
  * AZ-964: Fix permanent drift since support for the `blob_properties.restore_policy` property (point-in-time restore) in the Terraform provider AzureRM `v3.36.0`

# v7.3.0 - 2022-11-24

Changed
  * AZ-908: Use the new data source for CAF naming (instead of resource)

Added
  * AZ-891: Add Azure File authentication block (AD/AADDS)

# v7.2.0 - 2022-11-10

Fixed
  * [GH-2](https://github.com/claranet/terraform-azurerm-storage-account/pull/2): Enable logging only if queues are used/created

Changed
  * AZ-130: Module code improvements, bump `diagnostics` module for sub-entities
  * AZ-130: `network_bypass` is now set to `'Logging', 'Metrics', 'AzureServices'` by default

# v7.1.0 - 2022-10-21

Added
  * [GH-2](https://github.com/claranet/terraform-azurerm-storage-account/pull/2): Enable logging for Queue Services
  * AZ-869: Add file share properties related variables

Changed
  * AZ-846: Bump diagnostic settings module version

Fixed
  * AZ-869: Fix PITR & blob data protection conditions

# v7.0.1 - 2022-10-07

Fixed
  * AZ-865: Fix Soft Delete for NFS 3.0 with Blob Storage

# v7.0.0 - 2022-09-23

Breaking
  * AZ-840: Upgrade to Terraform 1.3+

Changed
  * AZ-839: Bump `diagnostics` module

# v6.2.0 - 2022-09-16

Added
  * [GH-1](https://github.com/claranet/terraform-azurerm-storage-account/pull/1/): Add CORS rules option

# v6.1.1 - 2022-09-02

Fixed
  * AZ-836: Fix `large_file_share_enabled` parameter when `account_kind = "BlockBlobStorage"`

# v6.1.0 - 2022-08-12

Added
  * AZ-820: Add `is_hns_enabled` parameter

Fixed
  * AZ-823: Fix NFS 3.0 support with Blob Storage

# v6.0.0 - 2022-08-05

Added
  * AZ-130: Module Azure storage account - first release
  * AZ-504: Adding diagnostic logging
  * AZ-515: Compatible with CAF Naming
  * AZ-615: Add an option to enable or disable default tags
  * AZ-717: Compatible with Terraform 1+ and AzureRM provider v3+
