---
layout: post
title: "Howto: Configure Wireless modems (MTS/Tata Photon) with Ubuntu?"
date: 07 May 2013
categories: Tips
comments: true
---

The people who tried to use wireless modem (generally called 3G dongles) with Ubuntu definitely will have a terrible experience I am sure.

I shall share some experience first and later you would find some interesting answers as well.

Your dongle device is not connected on Ubuntu as a mass storage device. Hence you can't copy the .deb file which contains the drivers required to run your (here I use MTS) modem

Second, you managed copy the deb file and double clicked to install. But your Software manager isn't allowing you to install it

Third, you're a geek. Googled something and managed find how to change the architecture of the package and give it a shot for installation. Yeah extract those file to a directory. Then change architecture parameter inside  `DEBIAN/control` from `i386` to `all` now save and run `dpkg -b dirname package.deb` and try your luck with the new package. It's not really working you're exhausted.

People working for open source projects are much smarter. They solve everyday problems of several humanbeings without expecting anything back.

Here's a thrilling finish for this story.
First of all, forget all the nonsense above if you're running Ubuntu 10.4 or above. You know, you can go for a driverless installation for your dongle and Ubuntu even gives you the default settings for your devices as well! How about that? Sounds great isn't it.

1. Open `Network Connections`
2. Click on `Add` button. Make sure your device is plugged in.
3. From the dialog box appears, choose `Mobile Broadband` as connection type
4. Click `Create` button
5. Your dongle name will appear on the drop-down combo box in most of the cases. (Otherwise give it a shot with `Any` option)
6. Now click on `Continue`
7. Choose your country from the list
8. Click `Continue`
9. Choose provider from the default list. If your provide is not listed, I am sorry I don't know how to fix it. Currently MTS, Reliance and Tata Photon are supported.
10. Finalize your settings Click on `Apply`
11. The default settings will be mostly correct. If it's different/not going through contact your vendor. Click on `Save` 
12. Now go to the `Network` icon there in the task bar on the top.
13. Click `Enable Mobile Broadband`
14. Now remove and insert the device and let the system detects it.
15. Click on the connection name appears under `Network` menu to connect.

Enjoy hassle free Internet without any nonsense drivers!

P.S The deb file I installed was not going through and the detection menu was stuck. You might need to depend on the vendor provided solution if the Ubuntu version is prior to 10.4. Hope you understand why the device was not detected as a mass storage device. Clueless? Leave it then. Happy browsing.

Do you think it's required to have screenshots? Post a comment if required.
