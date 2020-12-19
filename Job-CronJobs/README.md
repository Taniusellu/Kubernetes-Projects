  Job / CronJobs
-------------------
* A Job creates one or more Pods and ensures that a specified number of them successfully terminate. As pods successfully complete, the Job tracks the successful completions.
 When a specified number of successful completions is reached, the task (ie, Job) is complete. Deleting a Job will clean up the Pods it created.

A simple case is to create one Job object in order to reliably run one Pod to completion. The Job object will start a new Pod
 if the first Pod fails or is deleted (for example due to a node hardware failure or a node reboot).

You can also use a Job to run multiple Pods in parallel.
 
 * A CronJob creates Jobs on a repeating schedule.

One CronJob object is like one line of a crontab (cron table) file. It runs a job periodically on a given schedule, written in Cron format.

Caution:
All CronJob schedule: times are based on the timezone of the kube-controller-manager.

If your control plane runs the kube-controller-manager in Pods or bare containers, the timezone set for the kube-controller-manager container determines the timezone that the cron job controller uses.

When creating the manifest for a CronJob resource, make sure the name you provide is a valid DNS subdomain name. 
The name must be no longer than 52 characters. This is because the CronJob controller will automatically append 11 characters to the job name provided and there
 is a constraint that the maximum length of a Job name is no more than 63 characters.

CronJob
CronJobs are useful for creating periodic and recurring tasks, like running backups or sending emails. CronJobs can also schedule individual tasks for a specific time, 
such as scheduling a Job for when your cluster is likely to be idle.

Example
This example CronJob manifest prints the current time and a hello message every minute:



Job > Pod > generate-keys(100)      - one time job [oneshot-job.yaml]


<img width="583" alt="Screenshot_1567" src="https://user-images.githubusercontent.com/13994900/87060752-81026e80-c1d0-11ea-8a7a-d9264198a626.png">


