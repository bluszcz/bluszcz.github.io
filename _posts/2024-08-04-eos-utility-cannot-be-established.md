---
layout: single
title:  "EOS Utility Communication with the camera via USB cannot be established"
date:   2024-08-04 14:57:47 +0100
categories: canon osx
---

When connecting your Canon camera to your MacBook for the first time, you might encounter an issue where communication via USB cannot be established. 

![Progress](/assets/images/eoscamerabusy.jpg)

> Communication with the camera via USB cannot be established.
> Start EOS Utility after closing all the apps that communicate with the camera, and then turn on the camera again.

Something is currently blocking access to your camera, and you need to close all applications that might be using it (such as OBS, browsers, Zoom, etc.). However, resolving this issue may not be straightforward.

Please try the following command:

```
ps axu |grep ptpcamera
```

If you have a process running, it is likely a part of Image Capture responsible for communication with the camera. Unfortunately, this process restarts immediately after being killed. As a workaround, there is a simple bash command that can help:

```
while `true`; do ps aux | grep "[p]tpcamera" | awk '{print $2}'|xargs kill -9;done
```

When the script is running, try connecting your camera. It should work.

Originally I found this recipe on [Canon Forum](https://community.usa.canon.com/t5/Camera-Software/Trouble-Connecting-EOS-R8-to-EOS-Utility-on-a-Mac/td-p/428023).