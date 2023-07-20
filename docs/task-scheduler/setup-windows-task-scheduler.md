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

<summary>Step 4: In case your computer hasn't connect to a network yet</summary>

Sometimes your computer hasn't connected to a network before the **Rclone mount** fails, which will lead to the task stopping. To prevent this, we will make a trigger to trigger the task every time your computer connects to a network

1. In the <mark style="color:yellow;">**Trigger**</mark> tab, click on <mark style="color:yellow;">**New...**</mark>\
   ![](<../.gitbook/assets/Task Scheduler - Step 4 Pic 1.png>)
2. Set up like me:\
   <mark style="color:yellow;">**Begin the task:**</mark> `On an event`\ <mark style="color:yellow;">**Log:**</mark> `Microsoft-Windows-NetworkProfile/Operational`\
   <mark style="color:yellow;">**Source:**</mark> `NetworkProfile`\
   <mark style="color:yellow;">**Event ID:**</mark> `10000`\
   ![](<../.gitbook/assets/Task Scheduler - Step 4 Pic 2.png>)

But note that, the task will be triggered even if it has an internet connection or not 😐

</details>

<details>

<summary>Step 5: Run / Stop Task</summary>

* You can run or stop it immediately in **Windows Task Scheduler**\
  ![](<../.gitbook/assets/Task Scheduler manage Task start stop.png>)

<!---->

* Also, you can stop it via **Task Manager**

<!---->

* Every time your computer boots up, it will start Rclone mount before the user logon

</details>
