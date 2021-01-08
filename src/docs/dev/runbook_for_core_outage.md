
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


While most services can still be functional when core graphql service is interrupted, however 
there are a few configuration items to be set for edge to recover once graphql service is restored.
For example playback and output writer tasks can be retried at a later time; though the default values
may be too small for extended outage.  All the configuration items are expected to be set in the `edge.config`
table for the clusters -- note that this will need to be set across ALL clusters that connected to the same core.



| Function | Configuration Item | Note |
|----------|--------------------|-----------------|
| Delay of reprocessing of playback and output writer tasks | `controller` section,  `task.reprocessing.delay_in_seconds` | default is `300` (seconds).  For extended outage, this should be set to 50 to 75% of the expected outage in seconds.  Note there are the 3-day maximum age of the data for these tasks so the maximum should be < 2 days in seconds   | 
| Maximum number of retries for task reprocessing | `controller` section, `task.reprocessing.max_retries` | default is 3.  And can be left as is |
