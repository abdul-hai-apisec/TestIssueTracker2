APIsec

Triggers on-demand scans for projects registered in APIsec.

apisec-run-scan

This action triggers the on-demand scans for projects registered in APIsec. Once the scan is completed successfully, You can view the scan results from the project home page in APIsec Platform. The link to view the scan results is also displayed on the console on successful completion of action.
If you configure the Issue Tracker to GitHub Issues (see Auto Bug Management), the list of open vulnerabilities across all security scans executed within this project can be viewed and closed from the GItHub issues.
Inputs
apisec-username
Required The APIsec username with which the scans will be executed.
Note: You can create a new user on APIsec with 'ROLE_USER' privilege.
apisec-password
Required The Password of the APIsec user with which the scans will be executed.
apisec-scan-job
Required The id of the scan job to run.
apisec-region
Required  The location the scan will be executed in
Default is Super_1
apisec-environment
Required The id of the environment to run.
apisec-project
Required The id of the project for security scan.
Example Usage
  name: Trigger APIsec scan
  id: scan
  uses: actions/apisec-run-scan@v0.1.2
  with:
   	 apisec-username: {username}
   	 apisec-password: {password}
 apisec-scan-job: 8a8094b67b9ac59e017ba54183153cf8 
   	 apisec-region: Super_1 
 	 apisec-environment: 8a8094b67b9ac59e017ba5416f083b2e 
 apisec-project: 8a8094b67b9ac59e017ba5416f043b2c
 
Hiding your credentials from GitHub
  https://gist.github.com/raghubetina/0ab2baa497e1a97cdc3cde947c426251
 
