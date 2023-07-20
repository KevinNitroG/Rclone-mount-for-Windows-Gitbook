# Create batch script

{% hint style="info" %}
* The directory where the batch script locates doesn't matter, you can create it in any directory
* See more about Rclone command to use it as your demand 😪
{% endhint %}

<details>

<summary>Create a Batch script file</summary>

1. **Create** a batch file _(Ex: Mount.bat)_\
   ![](<../.gitbook/assets/Create a Batch script 1.png>)\
   ![](<../.gitbook/assets/Create a Batch script 2 Rename.png>)
2. Edit it and put the below script inside the batch file\
   _(Ex: Notepad, Visual Studio Code,...)_

{% code title="Mount.bat" overflow="wrap" lineNumbers="true" fullWidth="false" %}
```batch
:CHECK_CONNECTION
ping google.com -n 1 > nul
if %errorlevel% neq 0 (
    timeout /t 5 > nul
    goto CHECK_CONNECTION
)

start SilentCMD your_rclone_command_1
start SilentCMD your_rclone_command_2

timeout /t 2

taskkill /f /im SilentCMD.exe
```
{% endcode %}

3. Replace <mark style="color:purple;">`your_rclone_command`</mark> in the script above 👆. You can mount multiple remotes just enter after <mark style="color:orange;">**`start SilentCMD`**</mark> command

</details>

<details>

<summary>Copy script file path</summary>

Copy the **full path** of the script above for the below step

Ex: `D:Rclone mount/Mount.bat`

</details>

<details>

<summary>Explain the script <em>(Needn't to read 😐)</em></summary>

1. It will ping to `google.com`, if it fails, it will retry to ping until it successes
2. After pinging successfully, it will start **SilentCMD** to run all <mark style="color:purple;">`your_rclone_command`</mark>
3. After <mark style="color:orange;">2 seconds</mark> of waiting, it will terminate _(End task)_ all the **SilentCMD** itself

With **SilentCMD**, **Rclone** doesn't run under any terminal, cmd,... So after terminating **SilentCMD**, **Rclone** still works 😤

</details>

***

{% hint style="info" %}
And now you can click on the script to mount your remotes, but there still is a **cmd window** pops up and we need to make it run most silently. So, let's move to [create-shortcut.md](setup-shortcut/create-shortcut.md "mention") step
{% endhint %}
