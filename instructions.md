Draft

Install choco on windows
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

Install jmeter
choco install jmeter --version=5.4.3

Refresh shell
refreshenv

Install jmeter plug-in manager
Download the Plugins Manager JAR file https://jmeter-plugins.org/get/ and put it into JMeter's lib/ext directory. Then start JMeter and go to "Options" menu to access the Plugins Manager.

Clone sample application from https://github.com/Azure-Samples/nodejs-appsvc-cosmosdb-bottleneck
git clone https://github.com/Azure-Samples/nodejs-appsvc-cosmosdb-bottleneck.git

Deploy the sample app using the PowerShell script
 cd SampleApp
 .\deploymentscript.ps1
 
Once deployment is complete, browse to the running sample application with your browser.
https://<app_name>.azurewebsites.net

Onboard resources in Azure Monitor by configuring diagnostics settings (unless it's already automated via Azure Policy)
Run load test and review the "resiliency score" report.
