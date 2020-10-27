Trace the AzureRM Virtual Machine DSC Extension remotely
========================================================

            

This function is useful to trace the Azure DSC extension, especially in push mode.


# Show all statuses, including Meta Pushes


Trace-AzureRMDSCExtension -ResourceGroup AZE2-ADF-RG-D06 -VMName AZE2-ADF-D6-vmAD02  -StatusView 3


# Just show the DSC for the main configuration


Trace-AzureRMDSCExtension -ResourceGroup AZE2-ADF-RG-D06 -VMName AZE2-ADF-D6-vmAD02


You just need the **ResourceGroup **and **VMName**.


The loop is on 10 second intervals, so you can change that i you like.


Also if you names the DSC extension other than Microsoft.Powershell.DSC, then you can change the name of the extension.


**Regex on VMName are supported**


Trace-AzureRMDSCExtension -ResourceGroup AZE2-ADF-RG-D06 -VMName
**vmAD02 *** *


Trace-AzureRMDSCExtension -ResourceGroup AZE2-ADF-RG-D01 -VMName
**'JMP|SQL'**


*I added ErrorAction SilentlyContinue so if the VM Extension is not deployed you will not receive any error (once it is deployed it will return the info)*


 

 

Sample Output, from your PowerShell session to a Virtual Machine in Azure.


 

 

        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.
