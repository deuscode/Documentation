# LANDesk Guides

![by Peter Kay](https://github.com/deuscode) - contact@kaypeter.com
***

## Patch and Compliance

In this guide, I will show you how to create a repair task and configure the various options for the patch and compliance section on LANDesk. This guide assumes that you have already created and configured your agent settings and have a working LANDesk environment. If not, please refer to your organization's system administrator.
***

### Repair Task Procedure

1. Open the **_Management Console_**.

![Open Management Console](https://github.com/deuscode/Documentation/blob/master/src/Documentation/LanDesk/images/Open%20Management%20Console.gif)


2. Go to the **_Security and Compliance_** module and select **_Patch and compliance_**.

![Go to Patch and compliance](https://github.com/deuscode/Documentation/blob/master/src/Documentation/LanDesk/images/Go%20to%20Patch%20and%20Compliance.gif)


3. Types, Scopes, Filters:
Make sure to check your _types, scopes, and filters_. 
*_Vulnerability_ is strictly used to filter patches. 
*_Scopes_ are your created queries of devices `this may be different based on your organization's configuration`. 
*_Filters_ are created to filter in certain types of patches for a certain type of OS. `In this example, we are using Critical/High for all windows devices`.

![Check your filters](https://github.com/deuscode/Documentation/blob/master/src/Documentation/LanDesk/images/Check%20Filters.gif)


4. Right click on your Organization's _patch group_ and select _Repair..._

![Repair...](https://github.com/deuscode/Documentation/blob/master/src/Documentation/LanDesk/images/Repair%20Task.gif)


5. Repair Settings:
  * Under `Add targets`, select `Don't add targets at this time` because you will be able to do this later. It is always better to have that flexibility at the end. If you already have a query of devices, you may choose that instead.
  * You have an option of `Ignore maintenance window if specified`. This option ignores any of your organization's maintenance window (It is a window of time to install vulnerability patches. Any patch and compliance task that runs outside of this window will not run.). When you check this option, all patches will run immediately or during a specified time.

![Ignore Maintenance Window](https://github.com/deuscode/Documentation/blob/master/src/Documentation/LanDesk/images/Repair%20-%20Ignore%20Maintenance%20Option.gif)


6. Select your _Task type_. It is recommended to use `Policy-supported push` due to its versatility. `Policies` are purely client-initiated and will run any time/day the client connects to the _**Core Server**_ or **_CSA (Cloud Service Appliance)**_. This way, the _scheduled task_ will only have to run once and the rest of the task is left up to the clients, once they are powered-on and online.

![Select task type](https://github.com/deuscode/Documentation/blob/master/src/Documentation/LanDesk/images/Repair%20-%20Task%20Type.gif)


7. You can leave the schedule task unscheduled, start immediately, or start at a later date/time. Please be aware, if you leave the task unscheduled, you will need to run it manually or else it will be indefinitely idle.

![Schedule Task](https://github.com/deuscode/Documentation/blob/master/src/Documentation/LanDesk/images/Repair%20-%20Schedule%20task.gif)


8. Click on save and you should be directed straight to the **_Scheduled Task_** section.

![Scheduled Task Section](https://github.com/deuscode/Documentation/blob/master/src/Documentation/LanDesk/images/Repair%20-%20Save.gif)

9. You can rename the scheduled task to fit your requirements.

![Rename task](https://github.com/deuscode/Documentation/blob/master/src/Documentation/LanDesk/images/Scheduled%20Task%20-%20Rename.gif)

10. If you did not add targets initially, you may drag and drop clients into the scheduled task. These clients will then receive the policy and download any patches and install them.

![Drag clients to task](https://github.com/deuscode/Documentation/blob/master/src/Documentation/LanDesk/images/Scheduled%20Task%20-%20Drag%20Clients.gif)


11. If you ignored the maintenance window option, you may start the scheduled task immediately.

![Start the scheduled task immediately](https://github.com/deuscode/Documentation/blob/master/src/Documentation/LanDesk/images/Scheduled%20Task%20-%20Start%20Now.gif)


## Monitoring and Troubleshooting

While the task runs, you can monitor the progress through the scheduled task. You may need to refresh the task by pressing the “Refresh” button in the scheduled tasks window.

![Monitor](https://github.com/deuscode/Documentation/blob/master/src/Documentation/LanDesk/images/Scheduled%20Task%20-%20Refresh%20Monitor.gif)

To check patch installation failure reason or to see what patches have been installed, go to the device window at the top, look for the machine in question, right-click on the machine and select **_Security and Patch Information_**.

![Troubleshooting](https://github.com/deuscode/Documentation/blob/master/src/Documentation/LanDesk/images/Scheduled%20Task%20-%20Patch%20Troubleshooting.gif)
