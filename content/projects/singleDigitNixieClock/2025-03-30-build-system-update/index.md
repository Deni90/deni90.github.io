---
title: "Project setup & build system update"
date: 2025-03-30
categories: ["Firmware", "Development Tools"]
tags: ["ESP8266", "Arduino", "Makefile", "Project Setup", "Automation", "CI"]
summary: "Replaced PlatformIO with Git submodules and makefiles, simplifying project setup, build and flashing for the nixie clock."
---

While I am experimenting with the clock’s case, I am spending a lot of time idling. To make this spare time more productive, I decided to improve the project by ditching PlatformIO. I find PlatformIO to be a nice GUI tool for development, but I find it cumbersome for project setup. It requires a lot of manual steps to reach the point to be ready to build the firmware. You need to install the plugin in VS Code, setup the ESP/Arduino environment and get all the necessary libraries. Since we are humans, it is easy to forget something or introduce errors.

To solve this issue I opted to replace PlatformIO with a set of tools and ideas to automate this process.

First, I wanted to have full control of all project dependencies including the Arduino core. The main idea was to remove the dependency to the already installed Arduino setup on the host. This is solved with Git submodules. During the setup phase every dependency is being cloned to the thirdParty directory.

Then, I wanted to use makefiles for the build system. Makefiles may look complicated, but they are standing the test of time. IDEs and frameworks are coming and going… To make my life easier, I stumbled upon this project: [makeEspArduino](https://github.com/plerup/makeEspArduino)

makeEspArduino project simplifies the way of defining project’s Makefile. Just set a couple of variables and include the makeEspArduino.mk and that's it.

To simplify project setup even more, I created a simple setup.sh script. After cloning the repo you only need to call this script to setup the environment. This script will clone all the necessary third party libraries and setup ESP/Arduino environment. No IDE is required.

Here is how to setup the project:
```bash
git clone git@github.com:Deni90/singleDigitNixieClock.git
cd singleDigitNixieClock/firmware
./setup.sh
```

This is how to build and flash the project:
```bash
# Build the project
make
# Build and flash the project firmware
make flash
# Build and flash file system:
make flash_fs
```

To open a serial console
```bash
make monitor
```

It may be overkill, but this way the project can be easily setup on CI.