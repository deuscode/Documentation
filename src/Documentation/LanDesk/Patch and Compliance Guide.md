# LANDesk Guides

![by Peter Kay](https://github.com/deuscode) - contact@kaypeter.com


## Patch and Compliance

In this guide, I will show you how to create a repair task and configure the various options for the patch and compliance section on LANDesk. This guide assumes that you have already created and configured your agent settings and have a working LANDesk environment. If not, please refer to your organization's system administrator.


### Repair Task

1. Open the **_Management Console_**.

![Open Management Console](https://github.com/deuscode/Documentation/blob/master/src/Documentation/LanDesk/images/Open%20Management%20Console.gif)


2. Go to the **_Security and Compliance_** module and select **_Patch and compliance_**.

![Go to Patch and compliance](https://github.com/deuscode/Documentation/blob/master/src/Documentation/LanDesk/images/Go%20to%20Patch%20and%20Compliance.gif)


3. Make sure to check your _types, scopes, and filters_. _Vulnerability_ is strictly used to filter patches. _Scopes_ are your created queries of devices `this may be different based on your organization's configuration`. _Filters_ are created to filter in certain types of patches for a certain type of OS. `In this example, we are using Critical/High for all windows devices`.

![Check your filters](https://github.com/deuscode/Documentation/blob/master/src/Documentation/LanDesk/images/Check%20Filters.gif)


4. Right click on your Organization's _patch group_ and select _Repair..._

![Repair...](https://github.com/deuscode/Documentation/blob/master/src/Documentation/LanDesk/images/Repair%20Task.gif)

5. 
