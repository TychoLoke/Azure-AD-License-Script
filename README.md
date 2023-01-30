# Azure AD License Script
A PowerShell script that connects to Azure Active Directory, retrieves information on licensed users and the licenses assigned to them, and exports the results to an Excel file. This script is Authored by Tycho Löke.

## Prerequisites
- Microsoft Online Services Sign-In Assistant
- Azure Active Directory Module for Windows PowerShell (64-bit version)
- Export-Excel Module for Windows Powershell

## Usage
1. Connect to Azure AD using the Connect-MsolService cmdlet.
2. Retrieve information on licensed users using the Get-MsolUser cmdlet and filter the results to include only licensed users.
3. Use a loop to retrieve the licenses assigned to each licensed user using the Get-MsolUser cmdlet.
4. Store the user information, including display name, email, and assigned licenses, in an array.
5. Export the results to an Excel file using the Export-Excel cmdlet.

Notes
- The script includes a dictionary of product SKUs and their common names, which can be added to as needed.
- Change companyname for your Microsoft Company name so it can translate the SKU.
- The exported Excel file will be saved to the C:\ directory with the file name User-Licenses.xlsx.
- The worksheet name in the exported Excel file will be named LicensedUsers.

## Troubleshooting
- If you encounter an error connecting to Azure AD, ensure that you have installed the Microsoft Online Services Sign-In Assistant for IT Professionals RTW and the Azure Active Directory Module for Windows PowerShell (64-bit version).
- If you encounter an error exporting to an Excel file, ensure that you have the necessary permissions to write to the C:\ directory and that you have installed the Export-Excel module.

## License
This project is licensed under the MIT License. 
