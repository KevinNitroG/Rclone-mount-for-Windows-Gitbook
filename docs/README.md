# Rclone mount for Windows

## What's this?

* This is my way to use Rclone to mount remotes like in Linux `--daemon`

> You can read [rclone mount doc](https://rclone.org/commands/rclone\_mount/#synopsis) to know what is `--daemon` mean

## Why's this?

* When you use `rclone mount` command, you need to <mark style="color:red;">keep the cmd window open</mark>. If you <mark style="color:orange;">close it</mark>, Rclone will stop 💀
*   In this way, it doesn't show any log, cmd window and runs independently from any process

    ![Cloud storage mounted by Rclone](<.gitbook/assets/Windows Explorer Preview Cloud Storage.png>)<img src=".gitbook/assets/Task manager preview rclone.exe.png" alt="Rclone run without any parent process" data-size="original">

