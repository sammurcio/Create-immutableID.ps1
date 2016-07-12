# Create-immutableID.ps1

## SYNOPSIS

Create-ImmutableID.ps1 - Generate ImmutableID (base64 conversion) from GUID of specified AD user(s). 

## DESCRIPTION 

Generates an immutableID, base64 coversion of the GUID, of specified user(s). If more than one user is processed
it will generate a CSV file of results.  

## OUTPUTS

Single user output is output to the console, multi-user is output to a CSV file.

## PARAMETERS

- -Property

(Optional) Specifies what AD user property to match its value with the value specified in the PropertyValue paramenter.

- -PropertyValue

The value to use to locate AD user(s)

- -Filename

(Optional) Specifies the CSV file name to be used for the report.
If no file name specificed then a unique file name is generated by the script.

## EXAMPLES

> .\Create-ImmutableID.ps1 -PropertyValue smurcio@domain.com

Returns the immutableID for an AD user who's UPN is smurcio@domain.com

> .\Create-ImmutableID.ps1 -Property UserPrincipalName -Propertyvalue * -Filename IDs_All_users.csv

Returns a report with the immutableIDs for all users in the AD forest, saves report as specified.

## LINK

https://github.com/sammurcio/Create-immutableID.ps1

## NOTES

Written by: Samuel Murcio

## Find me on:

* LinkedIn:	https://www.linkedin.com/in/samuelmurcio

* Github:	https://github.com/cunninghamp

## Change Log

V1.00, 08/02/2015 - Initial version

V1.01, 09/28/2012 - Added filename parameter

V1.02, 10/16/2012 - Added functionality to search across all child domains within a forest

V1.03, 10/17/2012 - Added visibile progress bar

V1.04, 06/12/2016 - Improved search filter when specifying wildcard for propertyvalue
