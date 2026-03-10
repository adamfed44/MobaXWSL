# MobaXWSL
A short and easy guide on how to get desktop enviroments with MobaXterm (NOT SPONSORED)

<img width="1892" height="1006" alt="obraz" src="https://github.com/user-attachments/assets/524f6e8a-25ed-4c8b-a568-f164633ce81f" />

(fluxbox running in VcxSrv, with MobaXterm.)

First, get MobaXterm.

https://mobaxterm.mobatek.net/download.html

Get either Free or Pro, but if you just wanna do it quick, get Free.

Then, make sure you have WSL enabled. If not, then follow the guide here: https://learn.microsoft.com/en-us/windows/wsl/install

After you have WSL installed, make a new profile. (replace YN with your own distro name)

wsl --install --distribution Ubuntu-24.04 --name YN --version 2

Then open MobaXterm. You can optionally remove MobaDiff and MobaTextEditor, in C:\Program Files (x86)\Mobatek\MobaDiff\. On the left with "User Sessions", there should be your WSL Profiles.

Open it and do:

sudo apt update

Install the desktop enviroment of choice:

## Gnome

sudo apt install ubuntu-gnome-desktop

## XFCE4

sudo apt install xfce4

## LXDE

sudo apt install lxde

## KDE Plasma

sudo apt install kde-standard

## Cinnamon

sudo apt install cinnamon-desktop-enviroment

## MATE (not possible, if you know how, then contribute and paste it in)

sudo apt install ubuntu-mate-desktop

## Fluxbox (it's a window manager, but I call it a desktop enviroment)

sudo apt install fluxbox

Once you've installed your desktop enviroment, open up a X server, like Xming or VcxSrv (you can do it with the deafult MobaXterm one, but your windows will overlap with Linux. Open it up and in the MobaXterm type this:

export DISPLAY=127.0.0.1:0.0

(127.0.0.1 is the localhost in an normal ip adress format)

Then do the start command for your desktop:

## Gnome

gnome-session

## XFCE4

startxfce4

## LXDE

startlxde

## KDE Plasma

startplasma-x11

## Cinnamon

cinnamon-session

## MATE (not possible, if you know how, contribute and paste it in)

mate-session

## Fluxbox

fluxbox

