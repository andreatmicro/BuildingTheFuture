# Testing the Auto-scale feature

Note: For this part, the application needs to be running on a *Standard* App Service Plan.

## Create na Auto-scale condition:

1. Browse to the 'Scale out' blade;
2. Select 'Custom autoscale';
![GitHub Logo](/Images/CustomAutoScale.png)
3. On the Default setting, add 2 rules: one for Scale in and another for Scale out;
![GitHub Logo](/Images/ScaleIn.png) ![GitHub Logo](/Images/ScaleOut.png)

## Disable the ARR Affinity setting under 'General Settings' of the Configuration blade.

This needs to be done to ensure that requests are round-robined to all instances hosting your application
![GitHub Logo](/Images/Affinity.png)

## Run a Performance test:

1. Click 'Set Organization';
2. Create New DevOps Organization;
3. Click 'New' to create a Performance test;
4. Use following settings:

![GitHub Logo](/Images/PerfTest.png)

5. Test should start in around 15 minutes.


## Check Load on application and instances increasing over time:

Note: wait until the performance test has started for a couple of minutes:

1. On Overview blade select the Requests graphic: Check the amount of requests your application is getting;
2. Change metric to CPU percentage of App Service Plan Scope.
![GitHub Logo](/Images/CPUmetric.png)
3. Go back to app requests metric: Select Apply Splitting.
![GitHub Logo](/Images/Splitting.png)
4. Go to Over view blade: check the App Service Plan info.
![GitHub Logo](/Images/InstanceNumber.png)


Next hands on Lab: [Slots, Swaping and testing in prod](https://github.com/andreatmicro/BuildingTheFuture/tree/master/4.%20Slots%2C%20Swaping%20and%20testing%20in%20prod)
