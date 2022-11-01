# Regression Suite Automation Tool (RSAT) Test Execution
RSAT to be used to automate business processes and end to end User Acceptance Tests on D365 FSCM environmnt.
# Prerequisites
Connect to OS VPN through Check Point
1. User must have access to the Remote Desktop Connection to connect the VM (VWC845) >> enter username and password
2. The VM need to be configured to trust the connection to the environment
3. User must have admin right to enter password
4. User must generate a Personal Access Token (PAT) from ADO with full access (Save this somewhere as you will need this during config settings)
5. Access to FSCM test environment
6. Azure DevOps
#Getting Started
Having fulfilled the above Prerequisites >> Lunch RSAT from the Desktop
#Config Settings
Select the Settings icon to display parameters that will establish connection or synchronisation to Azure DevOps, Finance and Operations Test Environment and Run Settings
#Azure DevOps
Azure DevOps Url - Enter the URL for the D365 ERP Project
Access Token - Enter the Personal Access Token (PAT) you generated from ADO
Project Name - Select/Enter the name of the Project in ADO to be automatically detected by RSAT.
Test Plan - Select/Enter name of the Test Plan
#Finance and Operations Test Environment
1. Hostname - Enter the host name of the FSCM environemnt, which is the URL of the test environment where the RSAT connection will be pointed to and ignore the https:// prefix.
2. SOAP Hostname - usaually same as the Hostname for UAT environments and higher - tier sandbox environment.
3. Admin User name - Enter Test User name, which is the email address of the user that belongs to the same tenant in Ordnance Survey.
4. Thumbprint - Enter the authentication certificate:
 (67A01CAA4C007213F9ED8A288034C8E7AAC3E74C)
#To generate a new certificate
1. Select New (This will create and install a new authentication certificate)
2. Save the .cer file in a folder for records 
3. Message prompt - The certificate is installed in the local machine's trusted root store.
Company name - Select Company name
#Run settings
Working directory - create a folder to store test automation files in your local drive e.g C:\Temp\RegressionTool.
Default broweser - Select the browser for test execution e.g edge, chrome, IE.
