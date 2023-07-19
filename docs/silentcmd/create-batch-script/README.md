# Create batch script

{% hint style="info" %}
* The directory where the batch script locates doesn't matter, you can create it in any directory
* See more about Rclone command to use it as your demand 😪
{% endhint %}

<details>

<summary>Create a Batch script file</summary>

1. **Create** a batch file _(Ex: Mount.bat)_
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

3. Replace <mark style="color:yellow;">`your_rclone_command`</mark> in the script above 👆. You can mount multiple remotes just enter after <mark style="color:orange;">**`start SilentCMD`**</mark> command

</details>

<details>

<summary>Copy script file path</summary>

Copy the **full path** of the script above for the below step

Ex: `D:Rclone mount/Mount.bat`

</details>
