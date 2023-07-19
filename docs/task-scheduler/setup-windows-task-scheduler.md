---
description: Using Windows built-in Task Scheduler to run Rclone mount silently
---

# Setup Windows Task Scheduler

1. Open **Windows Search** _(<mark style="color:purple;">Windows + S</mark>)_\
   _Search for:_ <mark style="color:yellow;">`Task Scheduler`</mark>\
   ![](<../.gitbook/assets/Search for Task Scheduler.png>)
2. In <mark style="color:yellow;">**Task Scheduler Library**</mark>, click on <mark style="color:yellow;">**Create Basic Task...**</mark>\
   ![](<../.gitbook/assets/Task Scheduler 2.png>)
3. Create task's **Name** and **Description**\
   ![](<../.gitbook/assets/Task Scheduler 3.png>)
4. Choose <mark style="color:yellow;">**When the computer starts**</mark>\
   ![](<../.gitbook/assets/Task Scheduler 4.png>)
5. Choose <mark style="color:yellow;">**Start a program**</mark>\
   ![](<../.gitbook/assets/Task Scheduler 5.png>)
6. Enter your Rclone mount command\
   ![](<../.gitbook/assets/Task Scheduler 6.png>)
7. It will ask to move the arg into arguments field, choose <mark style="color:yellow;">**Yes**</mark>\
   ![](<../.gitbook/assets/Task Scheduler 7.png>)
8. Click on <mark style="color:yellow;">**Open the Properties diaglog for this task when click Finish**</mark>\
   ![](<../.gitbook/assets/Task Scheduler 8.png>)
9. Click on <mark style="color:yellow;">**Change User or Group...**</mark>\
   ![](<../.gitbook/assets/Task Scheduler 9.png>)
10. Click on <mark style="color:yellow;">**Advanced...**</mark>\
    ![](<../.gitbook/assets/Task Scheduler 10.png>)
11. <mark style="color:yellow;">**Find now**</mark>, choose <mark style="color:yellow;">**SYSTEM**</mark>, <mark style="color:yellow;">**OK**</mark> and <mark style="color:yellow;">**OK again**</mark> get to back to Task Properties\
    ![](<../.gitbook/assets/Task Scheduler 11.png>)
12. In the **Conditions** tab, untick <mark style="color:yellow;">**Start the task only if the computer is on AC power**</mark>\
    ![](<../.gitbook/assets/Task Scheduler 12.png>)
13. You can edit more in **Settings** tab...\
    ![](<../.gitbook/assets/Task Scheduler 13.png>)
