# Hi!

A lot of people asked me about my windows terminal (Powershell) looks and theme and how to customize it. Here i will try to give you a detailed description how you can customize your **PowerShell** but you can also use similar methods to your **Zshell** or any **Linux shell**. So let's get started. 
![Screenshot of customized PowerShell in terminal windows11 with tranparency on.](/img/posh.png)
<p style="text-align:center">Example of end results</p>
<br>
<br>

## 1. Install Windows Terminal
First of all you need to install <span style="color:green">**Windows Terminal**</span>. You can download it from [here](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab) or search it in **Microsoft Store**. It's built-in in windows 11. After you install it you can open it and you will see something like this:
![Screenshot of Windows Terminal](/img/wt_0.png)
<p style="text-align:center">Windows Terminal</p>
<br>

## 2. Get PowerShell
Now you need to get  <span style="color:green">**PowerShell**</span>. You can download it from [here](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell) or search it in **Microsoft Store**. Now you will be able yo select it in **Windows Terminal**. You can do it by clicking on the down arrow in the top bar and select **PowerShell**. If you don't see it in the menu, just restart it. Now you will see something like this:
 ![Screenshot of Windows Terminal with PowerShell](/img/wt_1.png)
<p style="text-align:center">Windows Terminal dropdown menu with PowerShell</p>
<br>

Now go to your terminal setting and set **PowerShell** as you default shell. Also set **Windows Terminal** as your default terminal. You can do it by clicking on the down arrow in the top bar and select **Settings**. Now you will see something like this:
 ![Screenshot of Windows Terminal settings](/img/wt_2.png)



<br>

## 3. Font 
Now you need to install a font that will support all the icons and characters that we will use. I use <span style="color:green">**Cascadia Cove Nerd Font Complete**</span>. You can download it from [here](https://www.nerdfonts.com/).
Download it and install. After installing restart your Terminal app and select **CascadiaCove NF** as your default font. You can do it by clicking on the down arrow in the top bar and select **Settings**. Now you will see something like this:

 ![Screenshot of Windows Terminal settings](/img/wt_3.png)
<br>

## 4. Install Oh My Posh
Now you need to install <span style="color:green">**Oh My Posh**</span>. You can do it by running this command in your terminal:
```powershell 
winget install JanDeDobbeleer.OhMyPosh
```
Read the Oh My Posh documentation [here](https://ohmyposh.dev/docs/).
<br>

After this restart Terminal app and edit $profile file. You can open $profile by running this command in your terminal:
```powershell
notepad $PROFILE
```
if you want to edit in VS Code run this command:
```powershell
code $PROFILE
```
Edit the $profile file and add this line:
```
oh-my-posh --init --shell pwsh --config ~/jandedobbeleer.omp.json | Invoke-Expression
``` 
If you want you can use my profile file and just replace it with yours. You can download it from this repo. Your $profile file will be diffrent. change the path and ajust your settings. You can find more information about $profile file [here](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_profiles?view=powershell-7.1). After changeing $profile file restart your Terminal app. Now you will see something like this:
 
<br>

## 5. Install Oh My Posh Themes 
Now you need to install <span style="color:green">**Oh My Posh Themes**</span>. You can do it from [here](https://ohmyposh.dev/docs/themes). I added the theme i use in this repo and you can download it from here. You can also create your own theme. You can find more information about themes [here](https://ohmyposh.dev/docs/themes). After you download the theme you want you need to import it. 

## 6. Terminal Icons 
Now you need to install <span style="color:green">**Terminal Icons**</span>. You can do it by running this command in your terminal:
```powershell
Install-Module -Name Terminal-Icons -Repository PSGallery
```
Read the Terminal Icons documentation [here]()
Add this line in your $profile file:
```powershell
Import-Module -Name Terminal-Icons
```
After this restart Terminal app. Now you will see something like this (your theme will look diffrent):
![Screenshot of Windows Terminal with PowerShell](/img/wt_4.png)

<br>

## 7. Install PsReadLine
<span style="color:green">**PsReadLine**</span> is my favourite. It will suggest you commands and autocomplete them depending on your previous commands. You can do it by running this command in your terminal:
```powershell
Install-Module -Name PSReadLine -Repository PSGallery -Force
```
Read the PsReadLine documentation [here](https://docs.microsoft.com/en-us/powershell/module/psreadline/?view=powershell-7.1).
Add this line in your $profile file:
```powershell
Import-Module -Name PSReadLine
```
I will suggest you to go and read a blog by Scott Hanselman about [PsReadLine](https://www.hanselman.com/blog/how-to-make-a-pretty-prompt-in-windows-terminal-with-powerline-nerd-fonts-cascadia-code-wsl-and-ohmyposh). He is one of my favourite internet people. He is a great developer and you can learn a lot from his videos. You can find his videos on [YouTube](https://www.youtube.com/c/shanselman/videos). 

## 8. Terminal Customization
Windows Terminal is very customizable. You can change the background, the font, the opacity, the color scheme and a lot more. You can find more information about Windows Terminal customization [here](https://docs.microsoft.com/en-us/windows/terminal/customize-settings/profile-appearance). You can also find a lot of themes [here](https://windowsterminalthemes.dev/). You can also create your own theme. You can find more information about themes [here](https://docs.microsoft.com/en-us/windows/terminal/customize-settings/color-schemes). I included my settings.json file in this repo. You can check it for refarence.  