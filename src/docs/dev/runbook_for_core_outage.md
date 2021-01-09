
# Edge Dependency on core

Edge services or engines that need core connection:

* CRON legacy scheduler to create jobs
* CRON job creation to create jobs
* CRON interval scheduler (not enabled)
* CRON scheduled job downloader to update scheduled jobs table
* Adhoc loop to pull job
* Engine loop to update engines / builds from core to edge
* UpdateTask sync to core
* Engines such as Playback for storing media segments for TDOs and Output Writers for writing back engine outputs
* CRON launching scheduled jobs
* Job creation plan ahead time (broken)
* CRON overal enable/disable switch


While most services can still be functional when core graphql service is interrupted, however 
there are a few configuration items to be set for edge to recover once graphql service is restored.
For example playback and output writer tasks can be retried at a later time; though the default values
may be too small for extended outage.  All the configuration items are expected to be set in the `edge.config`
table for the clusters -- note that this will need to be set across ALL clusters that connected to the same core.

 

| Function | Configuration Item | Note | Setting to prepare for outage | Reset after outage is finished |
|----------|--------------------|-----------------|--------|------|
| Delay of reprocessing of playback and output writer tasks | `controller` section,  `task.reprocessing.delay_in_seconds` | default is `300` (seconds).  For extended outage, this should be set to 50 to 75% of the expected outage in seconds.  Note there are the 3-day maximum age of the data for these tasks so the maximum should be < 2 days in seconds   | ||
| Maximum number of retries for task reprocessing | `controller` section, `task.reprocessing.max_retries` | default is 3.  And can be left as is |||
| Enable/disable CRON interval scheduler | `controller` section, `cron.interval_scheduler_enabled` | default is false, should be set to false |||
| Enable/disable CRON scheduled job downloader | `controller` section, `primary.cron.sched_job_downloader_enabled` | should be set to true |||
| Enable/disable CRON legacy scheduler | `controller` section, `primary.cron.scheduler_enabled` | should be set to true |||
| Enable/disable adhoc job downloader | `controller` section, `primary.cron.adhoc_enabled` | should be set to true |||
| Enable/disable all of CRON | `controller`, `primary.cron.enabled` | should be set to true |||
| Enable/disable CRON job creation | `controller`, `primary.cron.job_creation_enabled` | should be set to true |||
| Set CRON job creation SLOW channel plan ahead minutes | `controller`, `primary.cron.job_creation_slow_plan_ahead_min` | defaults to 180 (3h) |||
| Set CRON job creation FAST channel plan ahead minutes | `controller`, `primary.cron.job_creation_fast_plan_ahead_min` | defaults to 30 (30m) |||
| Set CRON legacy scheduler plan ahead minutes | `controller`, `primary.cron.scheduler.plan_ahead_min` | defaults to 180 (3h) |
| ??? | `controller`, `primary.engine_launch.enabled` | ??? |
| ??? | `controller`, `primary.update_stats.enabled` | ??? |
| ??? | `controller`, `task_status.enable` | ??? |




 
