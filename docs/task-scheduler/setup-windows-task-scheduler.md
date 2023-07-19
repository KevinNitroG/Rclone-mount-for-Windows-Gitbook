---
description: Using Windows built-in Task Scheduler to run Rclone mount silently
---

# Setup Windows Task Scheduler

<details>

<summary>Step 1: Open Task Scheduler</summary>

Open **Windows Search** _(<mark style="color:purple;">Windows + S</mark>)_\
_Search for:_ <mark style="color:yellow;">`Task Scheduler`</mark>\
![](<../.gitbook/assets/Search for Task Scheduler.png>)

</details>

<details>

<summary>Step 2: Create Task</summary>

1. In <mark style="color:yellow;">**Task Scheduler Library**</mark>, click on <mark style="color:yellow;">**Create Basic Task...**</mark>\
   ![](<../.gitbook/assets/Task Scheduler 2.png>)

<!---->

2. Create task's **Name** and **Description**\
   ![](<../.gitbook/assets/Task Scheduler 3.png>)

<!---->

3. Choose <mark style="color:yellow;">**When the computer starts**</mark>\
   ![](<../.gitbook/assets/Task Scheduler 4.png>)

<!---->

4. Choose <mark style="color:yellow;">**Start a program**</mark>\
   ![](<../.gitbook/assets/Task Scheduler 5.png>)

<!---->

5. Enter your Rclone mount command\
   ![](<../.gitbook/assets/Task Scheduler 6.png>)

<!---->

6. It will ask to move the arg into arguments field, choose <mark style="color:yellow;">**Yes**</mark>\
   ![](<../.gitbook/assets/Task Scheduler 7.png>)

<!---->

7. Click on <mark style="color:yellow;">**Open the Properties diaglog for this task when click Finish**</mark>\
   ![](<../.gitbook/assets/Task Scheduler 8.png>)

</details>

<details>

<summary>Step 3: Settings for Task</summary>

1. Click on <mark style="color:yellow;">**Change User or Group...**</mark>\
   ![](<../.gitbook/assets/Task Scheduler 9.png>)

<!---->

2. Click on <mark style="color:yellow;">**Advanced...**</mark>\
   ![](<../.gitbook/assets/Task Scheduler 10.png>)

<!---->

3. <mark style="color:yellow;">**Find now**</mark>, choose <mark style="color:yellow;">**SYSTEM**</mark>, <mark style="color:yellow;">**OK**</mark> and <mark style="color:yellow;">**OK again**</mark> get to back to Task Properties\
   ![](<../.gitbook/assets/Task Scheduler 11.png>)

<!---->

4. In the **Conditions** tab, untick <mark style="color:yellow;">**Start the task only if the computer is on AC power**</mark>\
   ![](<../.gitbook/assets/Task Scheduler 12.png>)

<!---->

5. You can edit more in **Settings** tab...\
   ![](<../.gitbook/assets/Task Scheduler 13.png>)

</details>

<details>

<summary>Step 4: Run / Stop Task</summary>

* You can run or stop it immediately in **Windows Task Scheduler**\
  ![](../.gitbook/assets/image.png)

<!---->

* Also, you can stop it via **Task Manager**

<!---->

* Every time your computer boots up, it will start Rclone mount before the user logon

</details>
