# Explain script

## Script

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

***

## Explanation

1. It will ping to `google.com`, if it fails, it will retry to ping until it successes
2. After pinging successfully, it will start **SilentCMD** to run all <mark style="color:yellow;">`your_rclone_command`</mark>
3. After <mark style="color:orange;">2 seconds</mark> of waiting, it will terminate _(End task)_ all the **SilentCMD** itself

{% hint style="info" %}
With **SilentCMD**, **Rclone** doesn't run under any terminal, cmd,... So after terminating **SilentCMD**, **Rclone** still works 😤
{% endhint %}
