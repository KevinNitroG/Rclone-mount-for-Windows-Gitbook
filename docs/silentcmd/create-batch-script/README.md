# Create batch script

{% hint style="info" %}
The directory where the batch script locates doesn't matter, you can create it in any directory
{% endhint %}

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

3. Replace <mark style="color:yellow;">`your_rclone_command`</mark> in the script above 👆

{% hint style="info" %}
See more about rclone command to use it as your demand 😪
{% endhint %}

4. Copy the **full path** of the script above for the below step

> Ex: `D:Rclone mount/Mount.bat`
