---
description: Made by Kevin Nitro 💖
cover: .gitbook/assets/windows 11 wallpaper.jpg
coverY: 0
---

# Rclone mount for Windows

## INTRODUCTION

Use Rclone to mount remotes like in Linux `--daemon`, or "daemonise" Rclone 🤔

{% hint style="info" %}
You can read [rclone mount doc](https://rclone.org/commands/rclone\_mount/#synopsis) to know what is `--daemon` mean
{% endhint %}

## WHY'S THIS?

<details>

<summary>Rclone mount in Windows needs cmd console</summary>

When you use `rclone mount` command, you need to <mark style="color:red;">keep the cmd window open</mark>. If you <mark style="color:orange;">close it</mark>, Rclone will stop 💀\
![Console while running Rclone mount](<.gitbook/assets/Preview - Rclone mount console.png>)

</details>

<details>

<summary>With this, it doesn't need cmd console, cmd window and run with parent process</summary>

![Cloud storage mounted by Rclone](<.gitbook/assets/Windows Explorer Preview Cloud Storage.png>)<img src=".gitbook/assets/Task manager preview rclone.exe.png" alt="Rclone run without any parent process" data-size="original">

But actually, there still is a **Windows host console** running while **Rclone mount** runs 😐

</details>
