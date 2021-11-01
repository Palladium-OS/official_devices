# **Palladium OS - Maintainership Details:**

![Image of Yaktocat](/rdmassets/bannerv1.1.jpg)

## **Official Support Guidelines & Rules:**

To become the official maintainer of Palladium OS, you need to submit a patch to Gerrit. You can find everything important related below.

## **Prerequisites**:

------

### **Please read the Prerequisites [**Here**](https://github.com/Palladium-OS/official_devices/blob/12/Prerequisites.md) before applying**.

-----

## ***How to apply!***

------

### ***1) Cloning the repository*** 

```bash
cd ~/
git clone https://github.com/Palladium-OS/official_devices.git -b 12 official_devices
```
------

### ***2) Add your device***


```bash
cd official_devices/devices
```

#### Open official_devices.json and add your device details. After adding your device details use [this](https://jsonformatter.curiousconcept.com/#) to format your JSON.

------

### ***3) Setting Gerrit (optional)***
#### Please read the Gerrit Setup guide [**Here**](https://github.com/Palladium-OS/official_devices/blob/12/gerrit/gerrit-config.md) if its your first time dealing with Gerrit.

------

### ***4) Staging***

```bash
cd ~/official_devices
git add .    
```
------

### ***5) Downloading commit-msg hooks***

```bash
gitdir=$(git rev-parse --git-dir); scp -p -P 29418 <YourGerritUserName>@mail.palladiumos.com:hooks/commit-msg ${gitdir}/hooks/    
```
#### ***Remember To replace ```<YourGerritUserName>``` with your gerrit username***
------

### ***6) Commit your changes***

```bash
git commit -m "official_devices: add <yourdevice codename here> 

Device Tree:

Kernel Tree:

Vendor Tree:

Reason for prebuilt kernel (if exists):

Telegram username:
"     
```
------

### ***7) Pushing your changes***

```bash
git push ssh://<YourGerritUserName>@mail.palladiumos.com:29418/Palladium-OS/official_devices HEAD:refs/for/12    
```
#### ***Remember To replace ```<YourGerritUserName>``` with your gerrit username***
------
------