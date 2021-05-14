This project will use a jar to build and deploy this into an environment. It will wait for an input from a user (probably a QA) to approve the deployment post build job.

The Jobs from jenkins are in /Project_Path/jobs folder. These jobs need to be altered post import into jenkins since the folder structure from where the jobs are exported is different.

The project makes use of antProj to build (create a jar) and deploy (execute the jar file created in build).

The BuildAndDeploy job also sends a mail to listed users once the build has been done to approve so deployment can be done. The job blocks till listed user approves the build to be deployed. Also, another mail is sent when the job is approved.

Next step is :
Resend a mail when the job has not been approved for 24 hours.
Probably try unblocking the agent till the job is waiting for approval.
