# Changelog

This is a list of changes in the most recent versions of the CLI.

All versions of the CLI are tested to be compatible with the matching version of the Morpheus Appliance. Backwards compatibility with older appliances should be preserved in most cases.

## 8.0.6

### Enhancements

* New command `storage-datastores` for managing storage datastores
* New subcommand `datastores add` for adding cloud datastores
* Updated `user-settings clear-access-token|regenerate-access-token` to support new option `--id ID` for clearing and regenerating a specific token by ID
* Updated `clients add` to support Redirect URI
* New subcommand `network-floating-ips` allocate for allocating network floating IPs
* Updated `clusters add` to improve Load Balancer input prompting

## 8.0.5

### Enhancements

* New command `backups restore` for restoring backup results to a new or existing instance
* New command `hosts list-devices|assign-device|attach-device|detach-device` for managing host device assignment

### Fixes

* Fixed `network-routers add` not prompting for Cluster for the OVS Bridge router type
* Fixed `hosts maintenance --deleteLocalData` not setting the request parameter correctly
* Fixed `hosts leave-maintenance` displaying the wrong message on success
* Fixed `license get` to display expired licenses as "(expired)" instead of a positive number of days

## 8.0.4

### Enhancements

* Updated `license get` to display all installed licenses
* Updated `license install|test` to work with stackable licenses using new options `--add` and `--replace`
* Updated `license uninstall` to support new option `--key KEY` for uninstalling a specific license key
* Updated `hosts maintenance` to support new options `--force`, `--deleteEmptyDir`, `--deleteLocalData` and `--deleteEmptyDir`

### Fixes

* Fixed `clusters add` not prompting for Resource Pool and Security Groups for MKS
* Fixed `clusters add --workflow` option using the wrong parameter name in the payload
* Fixed `networks add` not prompting for Network Domain for custom network types.

## 8.0.3

### Enhancements

* Updated `instances snapshot` to refresh process until complete and then show snapshot details

## 8.0.2

### Enhancements

* Updated `instances add` and `instances resize` volume configuration to prompt for Storage Controller Mount Point for `controllerMountPoint` parameter
* Updated `virtual-images convert` to prompt for options
* Updated `clusters update` to support new option `--useAgent on|off` for relaying Kubernetes communication through the agent
* Updated `clusters add-datastore|remove-datastore` to handle asynchronous API behavior

### Fixes

* Fixed interactive login prompting for commands run with `--dry-run` while not logged in
* Fixed `instances add` and `instances resize` volume configuration Datastore options not containing all the available options. Now it always loads them from `/api/data-stores`
* Fixed `library-cluster-layouts get` error. Using `id` worked but name or code caused an error
* Fixed `--select` so that it renders pretty json when used with `-j` eg. `instances get 42 --select volumes -j`
* Fixed `clusters add` for kubernetes on KVM causing an error trying to prompt for Resource Pool
* Fixed `history [search]` not showing the most recent commands when a search query is used

## 8.0.1

### Enhancements

New subcommand `virtual-images convert` for converting virtual image formats

### Fixes

Fixed `clouds add` prompting for credentials for standard cloud type

## 8.0.0

### Enhancements

* New subcommands `clusters add-datastore|remove-datastore|get-container` for managing cluster datastores
* New command `library-operating-systems` for managing library operating systems
* New subcommands `processes retry|cancel` for retrying and cancelling processes
* Updated `clusters update` to support new option `--autoRecoverPowerState [on|off]` and `clusters get` to display Auto Power On VMs
* Updated `backups` with better support of the different backup job types
* Updated `setup` to support new option `--license` and prompt for a License Key before the setup request
* Updated `license get` to display new license settings for socket limit and task types
* Updated `virtual-images add` to prompt for upload type file or url and prompt for URL/Path to set url and if url is used then create virtual image and file in one request instead of making the subsequent call to upload the file
* Updated `hosts update` to support new option `--ssh-key-pair` to set SSH Key

### Fixes

* Fixed `instances resize` including extra interfaces for multi server instances and creating duplicates. It no longer includes `networkInterfaces` in the payload by default since the API no longer requires it. There is a new option `--include-network-interfaces` to include the current network interfaces in the payload which may be used for older appliances or for help building a payload to add/edit interfaces

## 7.0.7

### Enhancements

* MVM Cluster type support

## 7.0.6

### Enhancements

* New command `servers maintenance|leave-maintenance` command for managing MVM host maintenance mode
* New command `servers maintenance` commands for managing MVM virtual machine server placement

### Fixes

* Fixed `provisioning-licenses` displaying Description twice
* Fixed `instances add` payload to include `ipMode=static` when `ipAddress` is passed
* Fixed `clusters add` payload to use `servicePlanOptions` instead of `plan.options` for custom plan options

## 7.0.5

* No major changes from 7.0.4.x

## 7.0.4.1-2

### Fixes

* Fixed gem install dependency issue with public_suffix

## 7.0.4

### Enhancements

* Updated `network-servers` to prompt for visibility and tenants
* Updated `execution-request execute` to support new option `--send-keys`

### Fixes

* Fixed several unit tests

## 7.0.3.1

### Fixes

* Fixed gem install dependency issue with ffi

## 7.0.3

### Fixes

* Fixed issue with `network-routers firewall-rule [router] [rule] --dry-run`

## 7.0.2.1

### Fixes

* Fixed `man` error

## 7.0.2

### Enhancements

* New command `email-templates` for managing email templates.
* Updated `budgets` to support Forecast Model

### Fixes

* Fixed issue with `clusters add` and the resource pool option type loading
* Fixed issue with `--curl` when the payload is a file and not 'application/json'

## 7.0.1

### Enhancements

* Updated `license get` to show license usage for new standard limits.

## 7.0.0

### Enhancements

* Updated `license get` to show License Usage containing bar graph for each limit and support new standard license limit type.

### Fixes

* Fix `catalog-item-types update-logo` not updating the logo

## 6.3.4

### Enhancements

* Updated `clouds` to support viewing and setting Labels
* Updated `groups` to support viewing and setting Labels
* Updated `groups list|get` to display the same information as the UI, including counts for Instances, Hosts, VMs

### Fixes

* Fix bug that prevented more than 1024 characters from being entered as a prompt input, for example on `license install` 'License Key:' prompt
* Fix `setup` license install printing deprecation warning about 'license apply' command
* Fix `networks list` showing inactive subnets as active

## 6.3.3

### Fixes

* Removed command `dashboard`

## 6.3.2

### Enhancements

* Updated `resource-folders update` to support `--default-folder on` and `-image-target on`

### Fixes

* Fix prompting for options that have `type=hidden` and use an `optionSource`
* Fix prompting for options that use the `requireOnCode` flag to determine if they are required
* Fix `resource-folders get` always showing Default: No
* Fix `catalog add` making an extra and unneccesary api request to `/api/catalog-item-types`

## 6.3.1

### Enhancements

* New command `library-cluster-packages` for managing cluster packages.
* New command `library-forms` for managing option forms and their inputs.
* Renamed `self-service` to `catalog-item-types`. The old command still exists, though it will be deprecated in the future. Please update your scripts to use `catalog-item-types`.
* Updated `catalog-item-types` to support forms.
* Updated `catalog` to support types that use forms. The CLI only supports prompting for the Basic input types, but support for all of the Advanced and Provisioning input types will be added soon.

### Fixes

* Fixed `certificates add --type nsxtCertificate` issue with the integration options not being provided for the Service prompt.

## 6.3.0

### Enhancements

* Updated `roles` to support Landing Url field named `landingUrl`

### Fixes

* Fixed `policies get-type` to allow the policy type name or id to be specified instead of requiring id

## 6.2.3

### Enhancements

* New command `network-servers` for managing Network Server integrations (NSX, etc)
* New subcommand `clusters refresh`
* New subcommand `clouds type` to view details about a specific cloud type
* Updated `clouds get` to display Last Sync and Sync Duration

## 6.2.2

### Enhancements

* Updated `catalog-item-type get` command to display `instanceSpec` as config in JSON format

### Fixes

* Removed `plugins check-updates` which is not yet implemented

## 6.2.1

### Enhancements

* Remove deprecated New Relic settings from `monitor-settings` command

### Fixes

* Fixed `roles update-catalog-item-type-access|update-report-type-access|update-vdi-pool-access|update-task-access|update-workflow-access` resulting in a 'Not Found' error for resources with access set to default
* Fixed `monitor-settings update` resulting in "Specify at least one option to update." error. This impacted several other commands as well

## 6.2.0

### Enhancements

* New command `backups` for managing backups
* Updated `instances` and `apps` to use new `displayName` property returned by the API
* Updated `instances run-workflow` to support new option `--phase PHASE`, and also `servers run-workflow`

## 6.1.2

### Enhancements

* Updated `instances add-schedule` to prompt for timezone
* Remove deprecated command `doc`

### Fixes

* Fixed `load-balancer-pools update` error

## 6.1.1

### Enhancements

* New command `load-balancer-pool-nodes` for managing load balancer pool nodes.
* Updated `roles get|list-permissions` to hide all resources with access set to `default`. There is a new option called `--include-default-access` to show all resource permissions, including default access.

### Fixes

* Fixed `cypher` so that item key is now now url encoded. This issue would occur when then item key contained a space or other special character.
* Fixed `instances add` and `networks add` network prompts not being scoped to the selected resource pool.

## 6.1.0

### Enhancements

* Updated `service-catalog add` to support new option `--payloads PATH`, providing a way to make many API requests with one command, one for each file matching the PATH pattern or directory. This option will become ubiquitous soon, and be available for all commands that already support --payloads.
* Deprecated option `payload-dir`. The old options will still work for now, but are hidden.

## 6.0.2

### Enhancements

* New subcommand `network-services refresh`
* Updated `service-plans` to support new options `--min|max-sockets` for Min/Max Sockets and `--min|max-cores-per-socket` for Min/Max cores per socket

### Fixes

* Fixed `instances add` issue with Resource Pool input always requiring a `pool-` prefix.
* Fixed `curl -XPOST --data` option not including the passed JSON data in the request.

## 6.0.1

### Enhancements

* Updated command `tasks execute` and `workflows execute` to support the new Instance Label and Server Label options. They also will now prompt for the context and target if --instances or --hosts are not passed
* Updated command `jobs execute` to support new Instance Label and Server Label options
* Lowered the default refresh interval from 10 to 5 seconds for commands `jobs execute`, `tasks execute`, `workflows execute`, `apps apply`, `instances apply`
* Updated `catalog` to support Quantity
* Updated `service-plans` options `--min-storage` and `--max-storage` label to 'Total Storage' and to always be in GB

### Fixes

* Fixed `process` and `jobs` table wrapping due to output and error values containing newlines.
* Fixed `instances add` requiring Resource Pool selection when provision type does not require it.

## 6.0.0

### Enhancements

* New command `resource-pool-groups` for managing resource pool groups
* New command `key-pairs generate` for generating key pairs
* New command `network-floating-ips` for managing floating ips
* New commands `containers attach-floating-ip|detach-floating-ip` for container floating ip management
* Updated `clusters add` to prompt for Floating IP
* Updated `apps remove`, `instances remove`, and `catalog remove` to support option `--release-ips [on|off]`. This replaces `--releaseEIPs`, which still exists as a hidden option. The CLI still sends both API parameters to accomadate new and older versions of the API.
* Updated `appliance-settings get|set` for new setting Stats Retainment Period
* Updated `catalog` and `self-service` for better support of the workflow item type.

### Fixes

* Fixed `roles update-global-*-access` commands to allow access value `custom`, which is still needed with API versions before 5.5.2.
* Fixed `apps get` error seen with apps containing multiple tiers
* Fixed `tasks execute` and `workflows execute` not supporting the `--quiet` option to suppress output

## 5.5.3.2

### Fixes

* Fixed `catalog add` prompting for option types out of order and not prompting for config options with dependent fields
* Fixed `login` prompt echoing password input after hitting enter (only seen on certain environments)

## 5.5.3.1

### Enhancements

* New command `network-server-groups` for managing network server groups
* New command `guidance-settings` for managing guidance settings
* New command `monitor-settings` for managing monitoring settings
* New subcommands `appliance-settings toggle-maintenance|reindex` for exeucuting admin utilities
* Updated `self-service get` to display catalog item Visibility and Layout Code

### Fixes

* Fixed `instances resize` and `hosts resize` volume size prompt using plan instead of current volume size by default

## 5.5.3

### Enhancements

* New subcommands `instances schedules|add-schedule|get-schedule|update-schedule|remove-schedule` for managing instance scaling schedules
* Updated `instances scaling` to display scaling schedules
* Renamed `instances scaling-update` to `instances update-scaling` and added support for option `--threshold ID` to use a source threshold scaling template.
* New subcommands `containers clone-image|import` for cloning and importing container images
* Updated `containers` (all commands) to support the standard request and output options
* New subcommand `hosts restart`
* New subcommand `clusters apply-template`

### Fixes

* Fixed `hosts resize` Plan default value not being set to the current plan
* Fixed lots of ruby warnings as a result of new unit tests

## 5.5.2.2

### Fixes

* Fix `roles list-permissions` error

## 5.5.2.1

### Fixes

* Fix `man` error

## 5.5.2

### Enhancements

* New command `security-packages` for managing Security Packages
* New command `security-scans` for managing Security Scans
* New command `plugins` for managing Plugins
* Updated `roles` permission access go along with system changes for the new default access and deprecation of "custom" value
* New subcommands `roles update-task-access|update-workflow-access` to manage RBAC for task and workflows
* Updated `users get` to add missing types of access such as `--report-types` and `--vdi-pools`
* Updated lots of commands with `--labels x,y,z` to adding/updating Labels and filtering on them
* Updated `networks` and `network-pools` for IPv6 support
* Updated `networks add|update` to support domain name instead of ID only eg. `--network domain.com`
* Updated `networks add|update` to support new option `--search-domains` to set Search Domains
* Updated `network-pool-servers` to go along with API updates
* Updated `library-instance-types` and `library-layouts` to support `--price-sets [LIST]` to set Price Sets association
* Updated `tasks` to support Visibility
* New subcommands `clients add|update|remove` for managing custom oauth clients
* New subcommands `integrations list-inventory|get-inventory|update-inventory` for managing Ansible Tower inventory permissions
* New subcommands `clouds update-logo|update-dark-logo` for managing custom logo icons
* New subcommands `library-instance-types update-dark-logo` for managing custom dark logo icons
* Updated `curl` to no longer use the system command so that it works on Windows now and also supports common remote options like --fields, --select, --yaml, etc.
* Updated `clouds remove` to support new option `--remove-resources`
* Updated `user-settings update` to support new option `--theme darkMode` for managing a user's UI theme

### Fixes

* Fixed `clouds add` not prompting for correct credential types for amazon/azure/google/softlayer
* Fixed `instance resize` service plan options for Openstack
* Fixed `library-node-types update --scripts 1,2,3` so it errors if an invalid script ID is passed
* Fixed `service-plans add|update` so that it allows passing 0 for max storage and memory
* Fixed `archives list-files bucket:/file/path` error
* Fixed `security-groups add-location` not prompting for customOptions based on type
* Fixed `apps add` so includes a `defaultCloud` parameter for other terraform/helm/arm blueprint types
* Fixed `instances add -t oraclecloud` not prompting for Availability Domain
* Fixed `monitor-alerts --apps x,y,z` causing an error

## 5.5.1.5

### Fixes

* Fix `price-sets list` error seen with new price types

## 5.5.1.4

This version corresponds to the release of the Morpheus API version **5.4.9**.

### Enhancements

* Updated `library-node-types add|update` to support new option `--evars name=value,name=value`
* Updated `clusters update` to support new options `--api-token TEXT` and `--managed [on|off]`

### Fixes

* Fix `instances add -t azure` not prompting for azure marketplace publisher/offer/sku/version.
* Fix `virtual-images add -t azure-reference` error when prompting for image.
* Fix `library-node-types add --templates LIST` being passed as scripts instead of templates
* Fix `users passwd` error when rendering result

## 5.5.1.3

* Fixed `deployments add-version` inconsistent input prompting

### Fixes

* Fixed `clouds add` getting stuck at username prompt seen for type VMware

## 5.5.1.2

### Fixes

* Fixed `clouds add` getting stuck at username prompt seen for type VMware

## 5.5.1.1

### Fixes

* Fixed `clouds add` error seen for type VMware related to new option type for credentials

## 5.5.1

### Enhancements

* New command `scale-thresholds` for managing Scale Thresholds
* New subcommand `clusters upgrade-cluster` to support MKS upgrade version upgrades
* Updated `roles add` and `roles update` to support updating any role permission and global access level such as `--permissions CODE=ACCESS`,`CODE=ACCESS`, `--global-group-access ACCESS`, `--instance-types CODE=ACCESS`,`CODE=ACCESS`, etc.
* Updated `clouds refresh` to add new support options `--mode costing --period 202206 --rebuild`
* Updated `tasks add` to prompt for credential
* Updated `library-option-types` (inputs) to support new "Verify Pattern" property
* CLI prompting for option type inputs now validates the `verifyPattern` regex pattern by matching it against the entire user input value
* Updated `library-node-types add|update` to support new option `--ports NAME=PORT`,`NAME=PORT`
* Updated `hosts remove`, `clusters remove` and `clusters remove-worker` to display a different success message that indicates when approval is required and the cluster/worker removal is now pending approval
* Updated `load-balancers get` with Price and Provider ID and removed SSL columns. Also tweaked `load-balancers add` as well
* Updated `clusters` to remove deprecated option `--display-name` and property `Display Name`
* Updated `clusters` to use the integrated credential option type to use a stored credential
* Updated `resource-pools` to support `Display Name` property

### Fixes

* Fix `library-node-types get --curl` causing an error
* Fix issue with prompting for some option types (inputs) that have `config.multiSelect: true` to support multiple values
* Fix `clouds refresh --mode costing --rebuild` error
* Fix `invoices line-items-list --all --wrap` still truncating Item ID
* Fixed `user-sources add` so that `--tenant` is no longer required and is also prompted for, also Default Role prompt works with ID or Authority now, also SAML type inputs are prompted for such as those under the SAML SSO Configuration and Role Mappings sections

## 5.5.0

### Enhancements

* Updated `clouds add` to prompt for credential
* Updated `tasks add` to prompt for credential
* Updated `library-option-lists add` to prompt for credential
* Updated `clouds add` to prompt for "Automatically Power VMs" (autoRecoverPowerState)

### Fixes

* Fixed `cypher get` not displaying data for responses that do not have a cypher item.
* Fixed `prices add --currency` so it uses the most recent list of supported currencies.
* Fixed `view cloud [id]` error

## 5.4.5.1

### Fixes

* Fixed man error

## 5.4.5

### Enhancements

* New commands `apps state` to view state information for Terraform apps
* Updated command `apps apply` to prompt for template parameters, use new validate-apply endpoint and also refresh until apply is complete
* New commands `instances apply` and `instances state` for Terraform instance types
* Updated command `clusters add` to support `--tags` and `--labels` options

### Fixes

* Fixed `catalog add` issue that caused option type list prompts to not work correctly
* Fixed `clusters add` issue with nodeCount parameter being required at server level too

## 5.4.4.2

### Fixes

* Fixed `catalog add` issue loading option lists values, `optionTypeId={id}` was not being included

## 5.4.4.1

### Fixes

* Fixed `instances clone-image` error due to `vmwareFolders` options source url change

## 5.4.4

### Enhancements

* New command `credentials` to manage Credential objects
* Updated `power-schedules` to support more granular times with `HH:MM` format (requires api 5.4.4)
* New subcommands `clusters update-worker-count|remove-worker` to change the number of workers or remove a specific worker
* Updated `self-service` to support new option `--dark-logo`

### Fixes

* Fixed `instances add|resize` prompting for root volume size when provision type does not support customization

## 5.4.3.1

### Fixes

* Fixed `instances add` error seen when plan has customizable memory but no default value defined

## 5.4.3

### Enhancements

* Updated command `instances add` and `instances resize` to prompt for plan customizations: Core Count, Cores Per Socket and Memory
* Updated `ping` and `remote add` to handle the API requiring authentication to retrieve `buildVersion`
* Updated `remote get` to no longer display `Appliance URL` since it is no longer returned
* Updated `virtual-images list` to support new option `--synced` and updated help to note "Default list applies User filter"
* Updated `library-instance-types list` to support new option `--featured`
* New command `snapshots` to manage Snapshots
* Removed command `instances remove-snapshot`. This has been replaced with `snapshots remove`

### Fixes

* Fixed `instances clone-image` to prompt for Folder when required (VMware)
* Fixed `networks` handing of `displayName`
* Fixed `tasks add` Retry Delay not persisting
* Fixed `clusters add` prompt for combo and docker types
* Fixed `tasks get` showing Script content incorrectly for Libray Script type

## 5.4.2

### Enhancements

* Updated command `load-balancers` to bring it up to date with the UI functionality
* New command `load-balancer-monitors` to manage Load Balancer Monitors
* New command `load-balancer-pools` to manage Load Balancer Pools
* New command `load-balancer-profiles` to manage Load Balancer Profiles
* Remove deprecated commands `integrations add-object|get-object|list-objects|remove-object`

### Fixes

* Fixed `image-builder add` issue with Preseed Script being required instead of optional
* Fixed `clusters add` issue with template parameters

## 5.4.1

### Enhancements

* New command `storage-servers` to manage Storage Servers.
* New command `storage-volumes` to manage Storage Volumes.
* New command `view` to open appliance resources in a web browser.
* New subcommands `instances refresh|apply` to plan and apply terraform instance types

### Fixes

* Fixed `clusters add` issue with template parameters

## 5.4.0

### Enhancements

* New command `network-edge-clusters` to manage Network Edge Clusters.
* New command `network-dhcp-servers` to manage Network DHCP Servers.
* New command `network-dhcp-relays` to manage Network DHCP Relays.
* New subcommands `roles update-global-report-type-access|update-report-type-access` to manage role report type access
* New subcommand `health export-logs` to download the appliance logs file

## 5.3.4

### Enhancements

* Updated `clouds list|get` to display Region Code
* Updated `instances clone` to prompt to keep existing metadata tags before adding new ones
* Updated `instances add|clone` changing the `metadata` parameter name to `tags`. The api has supported this since 5.0, when the response was renamed from metadata to tags

### Fixes

* Fixed `library-option-lists add --initialDataset "[]"` error caused by the parameter being converted to JSON instead of leaving it as a string
* Fixed `invoices list --totals` causing an error related to currency display
* Fixed `networks add` issue causing it to get stuck on Parent Network prompt
* Fixed `networks add` Network Pool prompt to be a select input
* Fixed `subnets add` error seen with Azure type
* Fixed `virtual-images list` so types are preloaded before output begins

## 5.3.3

### Enhancements

* Updated invoices to correspond with the 5.3 api to show invoice Currency and render amounts using the invoice source currency symbol.
* Updated library-cluster-layouts to support Install Docker option

### Fixes

* Updated dependency bundler version to ~> 2.2
* Fixed issue with clusters and the resource pool option type dependencies

## 5.3.2.3

### Fixes

* Fixed issue with instances resize -N -O dataVolume1.action=resize -O dataVolume1.size=42 not applying changes to payload as expected.

## 5.3.2.2

### Fixes

* Fixed issues with instances resize, -N would cause -O dataVolume1=42 to go unapplied, also made current plan the default selection and stopped rootVolume and dataVolume1 from being injected into the payload.

## 5.3.2.1

### Enhancements

* Updated networks and network-routers command for use with NSX-V and NSX-T requires api 5.2.9 or 5.3.3
* New command load-balancer-types command (replaces old load-balancers types command)
* Update tenants remove to support new option --remove-resources
* Deprecated commands log-settings enable_integration|disable_integration|remove_integration. The old options will still work for now, but are hidden.

### Fixes

* Fixed issue with some hidden commands still showing up in the manual and help output.
* Fixed issue with some option types that use the visibleOnCode property.

## 5.3.2

### Enhancements

* Changed library-option-lists get command to no longer display items by default, new option --items is available to load and display option list items. The 5.3.2 API changed to no longer return listItems

## 5.3.1.1

### Enhancements

* Changed invoices command to display Prices instead of Costs by default.
* New subcommands integrations list-objects|get-object|add-object|remove-object to fully manage ServiceNow integration exposed objects.

### Fixes

* Fixed issue with APIClient not respecting the setting :verify_ssl => false. This involved quite a bit of grooming to cleanup all the interface instantiation throughout used in the CLI commands.
* Fixed URI.escape is obsolete deprecation warning.

## 5.3.1

### Enhancements

* New command integrations to fully manage integrations.
* New command vdi-pools to support VDI Pool management.
* New command vdi to support VDI persona.
* Updated roles to support VDI Pool settings.
* New command certificates to manage SSL certificates.
* New option --select x,y,z for outputing only value(s). eg. instances get Test --select id or instances list --select id --newline " ".
* New option --delim [CHAR] and option --newline [CHAR] for get and list commands.
* Deprecated options --csv-delim and --csv-newline, use --delimiter and --newline instead. The old options will still work for now, but are hidden.
* Updated user-settings get to display Default Group, Default Cloud, 2FA Enabled, and Desktop Background.
* Updated user-settings update to support first class options for all the settings, including --avatar FILE.
* Update instances list to support new option --type CODE
* Update instances list to support new option --environment CODE requires api 5.3.1
* Updated reports exports to not require --format csv if the specified filename ends in .csv, now it is done automatically.
* New command hosts software-sync

### Fixes

* Fixed output of the --curl option for content types other than json, such as application/x-www-form-urlencoded and multipart/form-data. eg. output now uses -d for each parameter and -F 'user.avatar=@filepath for file uploads.
* Fixed error seen with instances list --fields id,name,status

## 5.3.0.3

### Fixes

* Fixed networks add --description
* Fixed network-domains add --type
* Fixed reports view

## 5.3.0.2

### Fixes

* Fixed `invoices list --cloud CLOUD` causing an error

## 5.3.0.1

### Fixes

* Fixed `service-plans add` error that would occur when prompting for resource permissions without multi tenancy

## 5.3.0

### Enhancements

* Updated `invoices refresh -c CLOUD` to have less options to correspond with the 5.3 api, which now always runs the hourly and daily costing jobs for the specified clouds for the current period. The option `--date=YYYY-MM-DD` allows processing invoices for a previous period (month).

* Updated `dashboard` and `activity list` to hide Resource column by default, `--details` will still display it.
* Updated `execution-request execute` to refresh every 5 seconds by default, instead of 30.

### Fixes

* Fixed `--all-fields` and `--csv` output so that objects are rendered in JSON format instead of Ruby format.
* Fixed `remove current` displaying Name value wrapped in `"`

## 5.2.4.1

This marks a shift in CLI version scheme. The CLI version is changing to match the semantic version of Morpheus appliance, so that the first 3 numbers will correspond to the appliance version release, and a fourth number will be used for CLI fixes that do not correspond to a release of the appliance.

### Enhancements
* Update `invoices` command to parse `lineItemCount` because `lineItems` is no longer returned with `invoices list`

### Fixes
* Fix option `--max -1`, since the server supports this, CLI also now supports `-m all` which pass `max=-1` in the request.
* Fix option `--sort x,y,z` to allow multiple fields since some endpoints now support this.

## 5.2.3

### Fixes
* Fixed `projects list -m` not working

## 5.2.2

### Enhancements
* New command `dashboard`
* Update `library-option-lists` to display and prompt for Help Block
* Update `history` usage to support arguments as `[search]` phrase
* Update `jobs list-executions` to support new option `--internal`
* Update `budgets` to support custom periods and new option `--costs LIST` replaces `--q1`, `--january`, etc.

### Fixes
* Fixed `curl [URL] --out /tmp/outfile.json` not writing to file

## 5.2.1

This version corresponds to the release of the Morpheus API versions **5.2.1** and **4.2.5**.

### Enhancements
* Renamed option for `instances [add|update] --metadata LIST` to `--tags LIST`. The API now expects `tags: [{"name":"color","value":"blue"}]` and Labels is now called `labels` instead of `tags`.
* New option `instances update --add-tags LIST`,  `--remove-tags LIST`, `--remove-tags LIST` to manage tags on instances.
* New option `hosts update --tags LIST`,  `--add-tags LIST`, `--remove-tags LIST` to manage tags on servers.

### Fixes
* Fixed `instances snapshots` not showing Description correctly
* Fixed `instances instances add --payload /path/to/payload.json --group GROUP` not applying group on top of payload.


## 5.2.0

This version corresponds to the release of the Morpheus API version **5.2.0**.

### Enhancements
* New command `catalog` for Service Catalog Persona: View catalog and manage inventory
* New command `self-service` for Self Service: View and manage catalog item types
* New option `instances list -a` as alias for `--details`
* New option `apps list -a` as alias for `--details`
* Updated `library-option-types get` to display associated Option List
* New option `virtual-images update --tags LIST`,  `--add-tags LIST`, `--remove-tags LIST` to manage tags on virtual images.

## 5.0.2

### Fixes
* Fixed `groups list --csv` not outputting groups as rows

## 5.0.1

This version corresponds to the release of the Morpheus API version **4.2.4**.

### Enhancements
* New command `search` that provides global search.
* New command `forgot` that provides forgot password email and reset.
* Updated `deployments list|add` to show more information and prompt for inputs.
* New subcommands `deployments list-versions|add-version|remove-version` for managing Deployment Versions
* New subcommands `deployments upload|remove-file` for managing Deployment Version Files.
* New command `deploys` for full management of instance deploys, including deploy of a new version to an instance with `deploys add`
* Enhancments for `deploy` command for using a morpheus.yml to creat a deployment, version and deploy it to an instance.
* Updated `instances list` to support new options `--tags Name=Value` and `--labels label`
* Updated `hosts list` to support new option `--tags Name=Value`
* Renamed option `--metadata` to `--tags`. old option still exists as a hidden option. The api still expects `metadata: [{"name":"color","value":"blue"}]`
* Updated several list commands to support search `[phrase]` as arguments 0-N instead of using `-s [phrase]`. This includes `instances list`, `hosts list`,`tasks list`, `logs list`, `health logs`. All commands should support this alternative soon.
* Updated `virtual-images add` to prompt for options required with type: Azure Reference. Prompts to search Azure Marketplace for publisher / offer and sku / version.
* Updated `curl` to support `-j` as an alias for `-p` (pretty JSON)
* Prompt for input type `code-editor` does not require user to tpe `EOF` any longer, just hit return.
* Hide options `--timeout` and `--header` since these are global options for any api request commands.
* Updated `whoami` output to display user ID first, and include Remote
* Updated `hosts list` and `hosts get` output to display status the same as instances and apps.
* Updated `hosts list` options: changed `-a` to `-a, --details`, renamed `-a, --account` to `--tenant`.

### Fixes
* Fix errors seen with `deploy` command.
* Fix error seen with `virtual-image get [id]`
* Deprecated `setup init`. This was removed some time ago, but wa still documented as a known subcommand. This command was renamed to just `setup`.
* Grooming of `man` content to bring it up to date.

## 5.0.0

This version corresponds to the release of the Morpheus API version **5.0.0**.

### Enhancements
* New subcommand `roles update-global-catalog-item-type-access`
* New subcommand `roles update-catalog-item-type-access`
* New subcommand `roles update-persona-access`
* Updated `roles get|add|update` for Default Persona
* Updated `user-settings get|update` for Default Persona
* New command `usage list`

## 4.2.22

### Enhancements
* Updated `resource-pools add-ip` to support `--next-free-ip` instead of always requiring `[ip]` to be passed
* Change `curl --data` option to set header `Content-Type: application/json` by default

### Fixes
* Fix `service-plans add` showing no available price sets
* Fix `jobs add --task` causing missing jobType error
* Fix `jobs add for --workflow` when option type is required, now prompts for optionTypes to populate customOptions object.
* Fix `curl --header 'Foo: bar` not working

## 4.2.21

### Fixes
* Fix `budgets add` error during prompting.
* Fix `tenants add` error during prompting.


## 4.2.20

### Enhancements
* Updated `resouce-pools update` to support `--default-pool [on|off]` option.

### Fixes
* Fix `library-instance-types add --option-types [x,y,z]` not working correctly.


## 4.2.19

### Enhancements
* Updated `tasks execute` to not require the `-a` flag.
* Updated `projects`  commands to support `--find-by-name` flag for finding projects with names that look like ids.

### Fixes
* Fix process event status `COMPLETE` displaying yellow instead of green.

## 4.2.18

### Fixes
* Fix error seen installing previous version on Windows, related to loading new RestInterface class

## 4.2.17

### Enhancements
* Updated `security-groups` to display the Active flag and it can be updated with `--active [on|off]`.
* Updated `invoices list` to display Tags and allow filtering with `--tags Foo=Bar --tags Hello=World`

### Fixes
* Fixed `instances update --group` not working.

## 4.2.16

### Enhancements
* Updated `invoices` command to support new option `--sig` and some other tweaks to the way data is displayed.

## 4.2.15

### Enhancements
* `library-option-types add` support for `--exportMeta` to `Export as Tag`.

### Fixes
* Fixed `tasks add add --no-prompt` still prompting for Content Ref. This fixes `spec-templates add` as well.
* Fix `library-option-types add` and `update` support for the `-O` option.

## 4.2.14

### Fixes
* Fixed `login -T` always resulting in *Token not valid* error.

## 4.2.13

### Enhancements
* Improved `logs list` output, the message output will flex to the width of the terminal and show more than one line, also new option `--table` is available. This also impacts `health logs` , `instances logs`, etc.

### Fixes
* Fixed `remote add --insecure` not working.

## 4.2.12

This version corresponds to the release of the Morpheus API version **4.2.1**.

### Fixes
* Fixed several issues with `invoices`.

## 4.2.11

### Fixes
* Fixed `ping` resulting in an error when used on older appliances. Now it falls back to use /api/setup/check instead of erroring.
* Fixed `remote setup` error and also improved error handling for `setup --remote-url` with an insecure url.

## 4.2.10

### Enhancements
* Prompt for credentials by default, instead of erroring. This was the behavior a long time ago, and now it is once again.
* Improved output of `remote list` and `remote get`
* Changed `remote get` to refresh status and version by default, can use option `--offline` to avoid this.
* Changed `remote get` to work like `remote current` when called with 0 arguments
* New subcommand `remote version`.
* New subcommand `remote view`.
* New command `setup` that works like `remote setup`
* New command `ping` that works like `remote check`
* New command `activity` that works like `recent-activity`
* Deprecated `recent-activity`
* Updated `instances` command renaming options `--created-by` to `--owner`
* Updated `apps` command to show Owner.
* Updated `blueprints` command to support Owner.
* Updated `blueprints` and `apps` command to show more information.
* Updated `invoices list -c CLOUD` so that name can be passed instead of just id.
* New option `apps update --owner`.
* Removed deprecated command `instances update-notes`.
* New subcommand `library-layouts update-permissions`.
* Changed the way role permission access values displayed, so they look more like a grid and full is green, while other values are cyan.

*Some of these enhancements require remote version **4.2.1** to behave properly.*

### Fixes
* Fixed error seen with `instances import-snapshot`
* Fixed `instances add` payload duplicating `plan`.
* Grooming of help info for `instances`, `apps` and `blueprints`.
* Fixed `--quiet` option still printing a newline.
* Fixed issues with `--remote-url` option, it could cause errors or otherwise behave incorrectly.
* Fixed issue with `instances add` using the wrong version when specified with `-O layout=ID` instead of `--layout ID`
* Fix `library-layouts get ID` 404 error incorrectly saying 'Instance Type not found'
* Fix `clouds add` not merging `-O` options into the payload
* Fixed `invoices` cost display issues

## 4.2.9

*Does not exist, skipped release 4.2.9 in favor of calling it 4.2.10*

## 4.2.8

### Enhancements
* New option `workflows list --type`.

### Fixes
* Fix `apps add` including `-O networkInterface` options when the blueprint has that field locked. This fixes potential serverside error 'ip address required'.
* Fix `users permissions` error when using older appliance versions.

*Some of these enhancements require remote version **4.2.1** to behave properly.*

## 4.2.7

### Enhancements
* New options `--wrap` and `--all-fields` for all `list` commands.
* New option `remote check --all` that works just like `remote check-all`.
* New option `curl -v`.
* Updated command `groups current` to support `--remote` option.
* Updated command `apps add` Environment prompt to be a select instead of text.
* Updated command `apps add` Environment prompt to be a select instead of text.
* Updated `apps list` and `apps get` to display Environment
* Changed *No records found* messages to be cyan instead of yellow.
* New option `--can-manage` for `security-groups add/update`.
* Changed `workflows get` to just show TASK ID in the tasks list, and no longer display ID ('taskSetTaskId').
* Renamed 'Tags' to 'Labels' in `instances get`
* Renamed option `--tags` to `--labels` for `instances add`.
* Added options `--labels` and `--metadata` to `instances add`
* Updated command `users permissions` and `users get --all` to show all access. *requires api 4.2.1*
* Updated command `whitelabel-settings` to support `--account` option. *requires api 4.2.1*
* New subcommand `clouds refresh`. *requires api 4.2.1*
* New command `guidance`. *requires api 4.2.1*

*Some of these enhancements require remote version **4.2.1** to behave properly.*

### Fixes
* Fix `apps add` not using blueprint values for layout,plan,networks,volumes,etc.
* Fix `apps add` not printing some error messages eg. 'name must be unique'.
* Fix `instances add --security-groups` causing invalid argument error.
* Fix `instances add` infinite *name must be unique* error when `--no-prompt` is used.
* Fix `passwd` extraneous output 'args is'.

## 4.2.4 - 4.2.6

### Fixes
* Fixes for new `invoices`  command.

## 4.2.3

### Enhancements
* Updated command `invoices` to show more info and make `--raw-data` an option.

### Fixes
* Fixed `clouds add` groups dropdown being limited to 25.
* Fixed multiselect option types not working when passed in eg. `--tenants "one, two"`

## 4.2.2

### Enhancements
* New command `invoices`

### Fixes
* Fixed `instances add` requiring Library permission to fetch layout.
* Fixed `instances add` requiring Clouds permission to fetch datastores.
* Fixed `instances add` potential 500 error when retrieving datastores.

## 4.2.1

### Enhancements
* New subcommand `service-plans activate`

### Fixes
* Fixed 404 error when fetching layout seen when pointing at appliance versions older than 4.2.  This change is to use /library instead of /libray/instance-types when for those resources.


## 4.2

This version corresponds to the release of the Morpheus API version **4.2**.

### Enhancements
* New command `network-routers`
* New option `networks add --group`
* New options `tasks add --source --url` for task types that supporting file-content instead of script content. ie. Groovy and Python
* Updated command `tasks get` with improved output format.
* New command `library-spec-templates`
* Updated commands `library-option-types`, `library-option-lists` by adding , `library-scripts`, and `library-file-templates` with prompting and standard option support.
* New option `library-instance-types add --option-types [x,y,z]`.
* New option `clusters add --worker-count N` and `clusters add-worker -n N`
* New option `service-plans update --active`.
* Updated `jobs add` to support `--schedule datetime --datetime DATE`.
* New option `instances add --ports ARRAY` and prompting for exposed ports.

### Fixes
* Fixed `tasks update --payload` not being supported.
* Fixed `prices add` and `price-sets add` prompts to match -O options
* Fixed `library-cluster-layouts add` prompts to match -O options
* Fixed `cypher put` not respecting `--key` and `--value` options

## 4.1.10

### Fixes
* Fixed `service-plans deactivate` missing confirmation prompt.

## 4.1.9

This version corresponds to the release of the Morpheus API version **4.1.2**.

### Enhancements
* New command `appliance-settings`
* New command `provisioning-settings`
* New command `whitelabel-settings`
* New command `log-settings`
* New command `approvals`
* New command `budgets`
* New command `health`
* New command `service-plans`
* New command `prices`
* New command `price-sets`
* Updated command `logs` output format to match more closely with the UI. This includes `logs list`, `instances logs`, `apps logs`, etc.
* Updated command `cypher put` to support more flexible format and store secret values as a string or object. Default TTL is now unlimited (0.)
* Updated command `workflows add` to create operational workflows, associate option types and to prompt for inputs.
* New subcommands `workflows execute` and `tasks execute`.
* Updated prompting to support `dependsOnCode` option type setting. This improves prompting for commands like `instances add` where irrelevant or duplicate option prompts could be seen.

### Fixes
* Fixed an error seen on Windows with select prompting.
* Fixed shell prompt still having ansi coloring with `shell -C` and after `coloring off`.
* Fixed issue with `-r [remote]` still using the previous remote's active group for `instances add`, `clusters add`, `apps add`.
* Fixed issue with the `-F`, `--fields` not excluding keys outside of the object scope. eg. `meta: {...}`.

## 4.1.8

### Fixes
* Fixed issue with monitor commands such as `mute` and `mute-all` displaying 'Unmuted...' instead of 'Muted...'.
* Fixed issue with `remote-url` option causing 'wrong number of arguments' error.

## 4.1.7

### Enhancements
* Updated `security-groups add` and `security-groups update` to support the options `--tenants`, `--group-access` and `--visibility`.

### Fixes
* Fixed issue with `subnets get -j` causing an error.
* Renamed `servers install-agent` to `servers make-managed` and added support for option `--install-agent off`.
* Fixed issue with `instances actions` causing an error.

## 4.1.6

### Enhancements
* New command `subnets` for managing network subnets. This replaces the commands that were named `networks *-subnets`.

### Fixes
* Fixed issue with `security-groups get` not displaying anything.
* Fixed issue with extra "Unexpected Error" being printed some typical errors.

## 4.1.5

### Enhancements
* New format for `-S, --sort ORDER` Sort Order. DIRECTION may be included as "ORDER [asc|desc]". Example: `instances list -S "dateCreated desc"`
* New command `clusters list-datastores|get-datastore|add-datastore` for managing cluster datastores. *Requires appliance version 4.2.0*
* New subcommand `monitor-incidents add`. *Requires appliance version 4.2.0*
* New command `appliance-settings`. *Requires appliance version 4.2.0*
* New command `monitor-alerts`. *Requires appliance version 4.1.1*
* Improved commands `monitor-contacts add`, `monitor-checks`, `monitor-groups` and `monitor-apps` by adding prompting.

### Fixes
* Fixed `roles update` to support the `--payload` option.
* Fixed issue with `instances logs`, `containers logs`, etc displaying records in the reverse order. Changed to match the UI.
* Fixed `instances view` and `apps view` only allowing one `[instance]` argument.

## 4.1.4

### Fixes
* Fix issue with `blueprints add-instance` that would not allow multiple instances of the same type for a tier.
* Fix issue with `blueprints add-instance-config` not prompting for Group, and instance can now be specified by name or index instead of just type.

## 4.1.3

### Fixes
* Fix issue with `instances clone` that would result in a 'Cloud not found' error when trying to use a shared/public cloud.
* Fixed an error that could be seen with select options having an Integer default value.

## 4.1.2

### Enhancements
* Improved `APIClient` so that is easier to use. See [APIClient](APIClient).

## 4.1.1

### Fixes
* Fix issue with `resource-pools add` resulting in no Group and Plan access. Now it passes `resourcePermissions.all=true` by default.

## 4.1.0

### Enhancements
* New command `clusters`
* New command `networks list-subnets|get-subnet|etc` for managing network subnets.
* New option `user-settings --user-id` for managing other users tokens,etc.
* Updated `roles add` and `roles update` to support the `--payload` option.
* New subcommand `containers logs`
* Select option prompts that have just one value are no longer skipped, and will now be seen with the only option selected as the default value.

### Fixes
* Fix issue with `library-option-lists update`  not allowing arbitrary `-O` options.
* Fix error seen with `library-node-type remove`.

## 4.0.0.1

### Fixes
* Fix issue with `instances history-event` breaking when an event had an error to display.

## 4.0.0

### Enhancements
* New command `wiki`
* New subcommands `network-pools list-ips|get-ip|etc` for managing network pool IPs
* New subcommands `network-domains list-records|get-record|etc` for managing network network domain records.
* Changed `--refresh` default interval to 30 seconds, instead of 5.


## 3.6.38

### Fixes
* Fix issue with `virtual-images add` to send imageType 'vmdk' instead of 'vmware'.
* Fix issue with `monitor-apps get` and `monitor-groups get` displaying Open Incidents as json

## 3.6.37

### Fixes
* Fix issue with `instances suspend` passing `server=true`

## 3.6.36

### Fixes
* Fix issue with `instances start-service` passing `server=true`

## 3.6.35

### Fixes
* Fix issue with download/export commands that use arrays as query parameter values

## 3.6.34

### Fixes
* Hide new `wiki` command until 4.0

## 3.6.33

### Fixes
* Fixed issue with `instances add -O instanceContext` option not being included in payload
* Fixed issue with `access refresh-token`

## 3.6.32

### Enhancements
* New command `reports`
* New command `instances view`
* New option `instances add --environment`
* New option `networks list -c [cloud]`
* Improved `instances clone` prompting
* New command `environments`
* New command `wiki`

### Fixes
* Fixed issue with `instances scaling`
* Fixed issue with `recent-activity` data parameters
* Fix issue with `library-node-types update` specifying atleast one option error with -O
* Fixed issue with `remote list` name column not being wide enough.
* Fixed `tenants` commands missing support for `--dry-run`, etc
* Fixed issue with `library-container-types add` needing `-O containerType.config={}`

### Deprecations
* Deprecated `instances firewall-enable and firewall-disable` which have been recently deprecated in the api.

## 3.6.31

### Fixes
* Fixed error seen with `instances resize` again

## 3.6.30

### Fixes
* Fixed error seen with `instances resize`

## 3.6.29

### Enhancements
* New command `resource-pools`
* New command `resource-folders`
* Updates to command `security-groups` for rule and location management.

### Fixes
* Fixed issue with `instances add`  requiring Resource Pool when there are none available.

### Deprecations
* Deprecated `security-group-rules`, replaced by `security-groups get|add-rule|remove-rule`


## 3.6.28

### Enhancements
* Updated `networks add` to have options for Network Domain and Proxy settings.

## 3.6.27

### Fixes
* Fixed issue with `library-node-types add` error generating 'Sorry, no options were found for provision type' for some types.

## 3.6.26

### Fixes
* Fixed issue with `apps add --blueprint` prompting for values that are already set in the config.
* Fixed issue with `apps add --blueprint -N` erroring with message about 'rootVolume.storageType' being required.
* Fixed issue with `apps add -N` erroring with message about 'Version' being required.

## 3.6.24

### Fixes
* Fixed issue with `curl --insecure` option having the typo 'inescure'.
* Fixed issue with `--curl` option output, copy + paste + enter not working, due to trailing ansi reset character.

## 3.6.23

### Fixes
* Fixed issue with `instances add` for Nutanix clouds not prompting for Datastore for volumes.
* Fixed issue with `instances add --layout` causing HTTP 500 error

## 3.6.22

### Enhancements
* Updated `alias` to allow [command] to be an expression.
* New option `morpheus -e` to execute an expression. This works just like `morpheus shell -e`.
* New option `benchmark exec -n` to run many iterations and print the average duration.

### Fixes
* Fixed issue with some commands exiting 0 when an error occurs.
* Fixed issue with `apps add` where JSON errors were not rendered nicely.
* Fixed issue with `hosts get ID` making a redundant api request.

## 3.6.21

### Enhancements
* New command `apps count`
* Added options to `instances count` and `hosts count`
* New command `hosts types` to list all server types via API.  *Required appliance version 3.6.2*

### Deprecations
* Removed command `hosts server-types [cloud]`. This has been replaced with `hosts types -c [cloud]`.

### Fixes
* Fixed issue with `apps list` having an extra newline in the output.

## 3.6.20

### Fixes
* Fixed issue with `apps add --validate` not displaying some errors, such as 'name: must be unique'.

## 3.6.19

### Enhancements
* Updated `instances list` to display a `CREATED BY` column.

## 3.6.18

### Fixes
* Fixed `history` command some more.

## 3.6.17

### Fixes
* Fixed `history` command behavior.

## 3.6.16

### Fixes
* Fixed `monitor-incidents list` `--status` and `--severity` options.
* Fixed `monitor-checks mute` Unexpected Error

## 3.6.15

### Fixes
* Fixed `groups use` causing unexpected error. This error was NOT seen when inside a morpheus shell, and likely impacted other commands too.

## 3.6.14

### Enhancments
* New options `instances list --details` to Display more details: memory and storage usage used / max values. `apps` and `hosts` have this option too.
* New option `tenants update --active [on|off]`

### Fixes
* Fixed `tenants update -O` not working.

## 3.6.13

### Enhancments
* Improved table display by preventing table wrapping. Only the columns that fit the terminal width will be displayed. This is enabled by default. If you want to see columns that are hidden because of terminal width, you can use `--all-fields` or `--fields x,y,z` option.
* Removed the *table_print* gem as a dependency.
* Changed usage of `tenants groups list -a [account]` to `tenants groups list [tenant]`.
* Improved `history` command. All prior commands are viewable now, instead of only the last 1000. History recording is now supported on Windows.

### Fixes
* Fixed `history` on Windows only displaying commands from current shell session.
* Fixed `clouds types` error.

## 3.6.12

### Enhancments
* Improved `history` command to support standard search `-s` and sort `-S` options.
* Changed `debug` command to work the same as `debug on`. The same goes for `coloring`.

### Fixes
* Removed extraneous debugging output with `cypher put`.
* Changed `cypher put` to put `ttl` in the query params and not the JSON payload.

## 3.6.11

* Improved `process list`, `process get`, `instances history` and `apps history` by truncating output by default. The new option `--details` can be used to see everything.
* New option `process list --app` for filtering by app(s).

### Fixes
* Fixed `cypher put` so that it skips the 'overwrite' confirmation prompt if the key does not exist already. It makes a list request beforehand to check if the key exists.
* Fix `apps security-groups-apply` causing Unexpected Error
* Fixed issue `history` command itself being logged consecutive times in the command history list.
* Fixed `man -gq` not being quiet
* Fixed a few help docs.


### Enhancements
* Fixed versioning to match current morpheus appliance version: `3.6.1`. Hopefully this avoid some confusion.

## 3.6.10

### Enhancements
* Finished adding support for `--curl`, `--timeout` and `--header` to all commands that should have it.
* Removed default 30 second timeout for `POST` and `PUT` api requests. Only `GET` requests will use the default 30 second timeout.  The new option `--timeout`  gives users a workaround as well.

### Fixes
* Fixed `whoami --dry-run` causing error.

### Deprecations
* Removed command `app-templates`. This has been deprecated and hidden since it was replaced with `blueprints`.

## 3.6.9

### Enhancements

**This release has so much!**

* Updated `cypher` command for simplified cypher key management. (requires appliance 3.6.0-2) The previous command that consumes the old cypher API is still available as the hidden command `old-cypher`. Please update your usage accordingly.
* Improved `login`. Refresh tokens are now stored with credentials to support refreshing.
* New command `access-token` that behaves like `whoami -t`
* New command `access-token refresh`.
* Updated `whoami` to
* New command `login --test` for testing credentials without updating the your session.
* New command `passwd` for changing passwords.
* New command `benchmark` to run adhoc benchmark tests for a command or series of commands. Also provides [on|off] commands to control the global benchmarking flag while in a shell.
* New option `-B` or `--benchmark` to print output about how long it took to run a command and the exit status.
* New option `--remote-url` for transient login with any command.
* New option `-U` or `--username` for transient login with any command.
* New option `-P` or `--password` for transient login with any command.
* Removed the short option `-B` from the `--keep-backups` option.
* New option `--curl` for doing a dry run that outputs a curl command that can be copy and pasted.
* New option `--header` to add extra headers to api requests.
* New option `--timeout` to use a custom timeout to api requests.
* note: `--header`, `--curl` and `--timeout` support is limited at the moment. It supported by a few several common commands eg. instances and apps. All will support it soon.
* Renamed `accounts` to `tenants`. The old command still exists, though it will be deprecated in the future.  Please update your scripts to use `tenants`.
* Updated `alias` command to improve help output and usability.
* Updated `--dry-run` output format to improve readability and usability. It  prints DRY RUN right away, before prompting, etc.
* Updated command `roles get` output to remove deprecated 'Role Instance Limits' settings. Also, moved global settings to details section to improve readability.
* Updated command `users get` output to remove deprecated 'Instance Limits' settings.
* New option `--thin` for less bulky headers and tables. At the moment,  support for this is...thin. A few popular commands fully support it eg. `instances`.
* Changed time format to no longer display the timezone ISO code. This was taking up extra space on some already too-wide tables.  We can add a timezone setting to the cli soon.

### Fixes
* Fix `groups list` missing support for `--dry-run`

## 3.6.8

### Fixes
* Fix issue with custom shell prompts not showing username after logging in.

## 3.6.7

### Fixes
* Fix issue with `apps` status displaying empty instead of PROVISIONING.

## 3.6.6

### Fixes
* Fix issue with `instances start` support of `-y` option.

## 3.6.5

### Enhancements
* Updated `instances stop|start|restart|etc` to accept multiple instance arguments.
* Updated `hosts stop|start` to accept multiple host arguments.
* Added confirmation to `instances start`, and support of Auto Confirm `-y` option.
* Added confirmation to `hosts start`, and support of Auto Confirm `-y` option.

## 3.6.4

### Enhancements
* Updated `apps add` to merge blueprints into payload and prompt for instance configuration.
* New option `apps add --validate` to only validate without creating.
* Replaced `apps add --config` options with standard `--payload` options.
* Replaced `blueprints add --config` options with standard `--payload` options.
* Updated `blueprints add` to prompt for type.
* New commands `apps stop|start|restart`
* New option `--payload-dir` for all commands supporting `--payload`.
* New option `--prompt` for all commands supporting `--options`.

### Fixes
* Fix issue with `apps add` not showing useful error messages.

## 3.6.3

### Fixes
* Fix issue with `apps add` not including `-O` options

## 3.6.2

### Fixes
* Fix issue with `run-workflow` requiring parameters

## 3.6.1

### Fixes
* Fix issue with archives upload timing out for large files

## 3.6.0

### Enhancements
* New commands `monitor-checks mute-all`

### Fixes
* Fix issue with `roles update-cloud-access` when group has to be specified
* Fix issue with `roles update --multitenant off`

## 3.5.3

### Enhancements
* New command `blueprints` to replace `app-templates`. The old command still exists, though it will be deprecated in the future.
* New command `instances history`
* New command `instances exec`
* New command `user-settings`
* New command `process`
* New command `execution-request`
* Change `instances add --workflow` to support Name or ID
* New filter option `tasks list --types`
* New filter option `servers list --account`. Servers finds records for all tenants by default for master tenant users.
* New command `roles update-global-blueprint-access` and `roles update-blueprint-access`
* New command `hosts update`

### Fixes
* Fix cloud status display not showing DISABLED.
* Fix issue with `--refresh-until [status]` never stopping.
* Fix issue with `--nocolor` not resetting between shell commands
* Fix issue with `remote add` always asking for login credentials twice.

### Deprecations

## 3.5.2

### Enhancements
* Updates to `instances list` and `instances get` to consume new api format for stats and load balancer data (no longer need to stitch together)
* New options for `instances update` to update metadata, power schedule, and group
* Renamed `storage-providers` to `storage-buckets` to correspond with API changes.
* The `--remove-volumes` option has been replaced with `--preserve-volumes` to correspond with API changes.
* `login` now prints 'Logged in to %remote as %username' on success
* New option `--refresh-until [status]` for `instances get`, `apps get` and `servers get`.

## 3.5.1.3

### Fixes
* Fix error output for `whoami -T [token] -j`

## 3.5.1.2

### Enhancements
* Renamed power-scheduling to `power-schedules` and mapped to new api endpoint
* Added new command `execute-schedules`
* Added new option `curl --pretty`
* Updated `curl [url]` to allow an absolute URL to allow easier copy and pasting

### Fixes
* Fixed issue with `shell` log-level being saved for subsequent commands when using `--debug` while in a shell
* Fixed some errors seen with power schedules

## 3.5.1.1

### Fixes
* Fixed issue with `storage-providers add -t rackspace`

## 3.5.1

### Enhancements
* New command `cypher` for managing cypher keys
* Updated `library-option-lists` to support the Source Headers settings
* Updated `storage-providers` file browser commands
* Updated `clouds` to display the Enabled setting
* Updated `set-prompt` to no longer reset to terminal default colors for input. Append `%reset` to your prompt string to keep that behavior.

## 3.4.1.10

### Fixes
* `instances update` should allow any option with `-O`

## 3.4.1.9

### Fixes
* Allow removing tasks still in use with `tasks remove --force`

## 3.4.1.8

### Fixes
* Fixes for `virtual-images add`

### New Dependencies
* Ruby version >= 2.3 is now required. This is for the http gem.

### Enhancements
* Improve performance of `virtual-images add`
* Improve performance of `virtual-images add`

### Fixes
* Allow task phase to specified for `workflows add --tasks`
* Fix error seen with `whoami -j`

## 3.4.1.4

### Enhancements
* New option `login -T` to login with an existing access token instead of a username and password

## 3.4.1.3

### Fixes
* Fix issue with `--fields` resulting in 'null' for values that should be 'false'.

## 3.4.1.2

### Fixes
* Fix issue with `--fields` resulting in 'null' for values that should be 'false'.

## 3.4.1.1

### Fixes
* Fix error with `policies` command.

## 3.4.1

### Enhancements
* New command `datastores` for managing cloud datastores
* New command `accounts groups` for managing subtenant groups

### Fixes
* Fix `--fields` option for lots of `list` and `get` commands

## 3.3.2.6

### Enhancements
* Enhanced expression parsing for `morpheus shell`. Parenthesis can be used in conjuction with operators. eg. `(whoami || login) && (instances list -m 5; hosts list -m 5)`

## 3.3.2.5

### Enhancements
* Updated `clouds list` supports more standard options
* Updated `clouds get` supports multiple arguments
* Updated `clouds add` and `clouds update` to support the `--payload` option.

### Fixes
* Fix issue with `clouds add` not including the default `config.certificateProvider` value, which the 3.3.2 api (incorrectly) requires.

## 3.3.2.4

### Enhancements
* `instances add` has new options `--name`, `--create-user` and `--user-group`
* `instances add` uses `--create-user=on` by default
* `instances add` will combine options on top of `--payload`

## 3.3.2.3

### Enhancements
* Improved commands `workflows` and `tasks`
* New commands `edit-profile` and `edit-rc`
* Removed `--json-raw` from help output.

## 3.3.2.2

### Fixes
* Fix issue with `library-file-template add --file`.

## 3.3.2.1

### Enhancements
* `morpheus` now parses pipe `|` input as command arguments. eg. `cat my_host_ids.txt | morpheus instances get`

## 3.3.2

### Enhancements
* New commands `library-*` to replace old `library` command
* New command `user-sources`
* Improved option `-F --fields`. You can now use field `as Label` eg. `--fields "id,name,plan.id as planId"`
* New option `-Q --query` for several `list` commands. This allows filtering with arbitrary query params.
* `shell` now supports simple use of `||` and `&&` operators
* New option `shell -e` for executing shell scripts
* New option `shell -Z` for Incognito mode
* New utility commands `edit-profile` and `edit-rc` and `sleep`

## 3.2.0

### Enhancements
* New commands `monitor-groups`, `monitor-groups`
* Renamed command `checks` to `monitor-checks`
* Renamed `incidents` to `monitor-incidents`
* New command `user-groups`
* New command `users passwd`
* Updated `users` commands to support `--payload` options

## 3.1.2

### Enhancements
* New command `storage-providers`
* New command `networks`, `network-groups`, `network-pools`, and others
* New option `--payload FILE` and `--payload-json JSON` for `instances add`

### Fixes
* Fix issue with `instances add` showing details after provisioning.

## 3.1.0

### Enhancements
* Changed format of command `instances add`. The old format of `instance add [type] [name]` is deprecated. The new format is `instances add [name] -t TYPE`
* Updated command `instances add` for 3.0
* Updated command `app-templates` for 3.0
* Updated command `apps` for 3.0
* New command `image-builder`
* New command `archives`

## 2.11.3.4

### Enhancements
* `virtual-images` command uploads without multipart.

### Fixes
* `roles update-feature-access` should allow any access value eg. 'user' or 'view'

## 2.11.3.3

### Fixes
* Fix issue with `remote setup --insecure`

## 2.11.3.2

### Fixes
* IP Address (optional) when using networks with IP Pools or DHCP.

## 2.11.3.1

### Fixes
* Fix issues with `remote add --insecure` and `shell --insecure`

## 2.11.2

### Enhancements
* New options for `instances add`. Automation inputs such as workflow, shutdown days, create backups, metadata.
* New command `recent-activity`

### Fixes

## 2.11.1

### Enhancements
* New command `containers action|actions|get|reject|restart|start|stop|suspend`
* New command `instances containers` and `instances get --containers`
* New command `instances scaling` and  `instances --scaling`
* New command `instances scaling-update`
* New command `instances action|actions`

### Fixes
* Fix `load-balancers add`
* Fix issue with Virtual Image prompt being optional when provisioning a private image.
* Fix issue with whoami --remote

## 2.11.0

### Enhancements
* Improved `remote` commands. Added `remote get`, `remote check`. Remote appliance status and session activity can now be seen.
* New command `incidents` for managing monitoring incidents.
* New command `checks` for managing monitoring checks.
* New options `--csv` and `--fields`.  Only available for `hosts` and `instances` at the moment.
* New commands `library option-types` and `library option-lists`
* New command `whoami -t` to print your access token only.
* New command `curl` for adhoc api testing.
* New command `man` for viewing the [CLI-Manual](CLI-Manual).
* Formatting changes for Details output, aligned and right justified labels.
* Formatting changes for `--help` output.

### Fixes
* Fixed missing command `instances logs`
* Errors are now written to STDERR.

## 2.10.3

### Enhancements
* Network Domain selection during instance and server provisioning

### Fixes
* Fix error seen when $HOME/.morpheus directory does not exist yet.
* Fix bug with `alias` not being available right away within a shell
* Fix some behavior with the shell's `history`, `!`  `!!` commands

## 2.10.2

### Enhancements

* Proper `.morpheusrc` file support for the shell.  You can put any morpheus command in here now.
* Support for `.morpheus_profile` and disabling it with the `--noprofile` option.
* Aliases need to be exported with `-e` or `alias export`, which stores them in the .morpheus_profile file.
* new script commands: source, echo, ssl-verification, coloring, log-level
* The `--debug` option now prints every API request that morpheus makes, and http response code. You can also turn this on all the time automatically in your .morpheus_profile with `log-level debug`
* Added `hosts make-managed`

### Fixes
* Fix a bug seen with Azure provisioning.
* Fix `shell --insecure` not working
* Fix `hosts upgrade-agent`
* Fix `instances clone`

## 2.10.1

### Enhancements

* Renamed the subcommand `details` to `get` for all commands. Use `hosts get "myhost"` instead of `hosts details "myhost"`
* Prettier usage stats for `instances get`, `hosts get` and `apps get`
* Display more information about `groups` and `clouds`  e.g. Clouds assigned to group, # of Hosts
* Added `groups add-cloud` and `groups remove-cloud` for managing which clouds are assigned to a group
* Added new `instances` commands `suspend`, `eject`, `console` and `status-check`
* Environment Variable configuration for `instances add`
* New options `--copies` and `--layout-size` for `instances add`
* Description, Environment, Tags options for `instances add`
* Added `remote setup` to [Setup New Appliance](Setup-New-Appliance)
* Support for the `-r` `--remote` option on just about every command
* Added `virtual-images` command for Virtual Image management
* Better [Morpheus Shell](Shell) performance and functionality
* Added [Morpheus Alias](Alias)
* Improved option parsing for all commands.  e.g.  [name] argument may appear before or after option switches
* Improved help documentation for all commands
* Make `list` the default subcommand for many commands. Now `hosts` can be used in place of `hosts list`.  This is experimental, and may be removed in 2.10.2
