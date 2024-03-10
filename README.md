# AWS CloudFormation Template for Patching Automation

This CloudFormation template automates and manages patching activities using AWS Systems Manager across dev and prod environments.

## Parameters
- **Name**: Name of the maintenance window.
- **RebootTagKey**: Tag key for rebooting instances.
- **RebootTagValue**: Tag value for rebooting instances.
- **MaxConcurrency**: Maximum number of instances to reboot simultaneously.
- **PatchingTagKey**: Tag key for patching instances.
- **PatchingTagValue**: Tag value for patching instances.
- **PatchingTaskType**: Type of patching task.
- **CronSchedule**: Cron schedule for maintenance window.
- **ScheduleTimezone**: Timezone for maintenance window schedule.
- **CreateSSMDocument**: Option to create SSM documents.

## Resources
- **SSMMaintenanceWindow**: Defines the maintenance window.
- **SSMMaintenanceWindowTarget**: Specifies targets for patching.
- **SSMMaintenanceWindowRestartInstancesTarget**: Specifies targets for instance reboots.
- **SSMMaintenanceWindowPatchingTask**: Defines patching tasks.
- **RebootTask**: Defines reboot tasks.
- **RenameTask**: Defines tasks for renaming credential files.
- **RenameBackTask**: Defines tasks for renaming credential files back.

## Usage
1. Deploy the CloudFormation stack using the provided YAML template.
2. Configure parameters according to your requirements.
3. Validate the deployment status.
4. Execute patching and maintenance tasks through Systems Manager.

## Disclaimer
This template is provided as-is, without warranties or guarantees. Use at your own risk.

