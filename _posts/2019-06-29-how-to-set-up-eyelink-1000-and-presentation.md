---
layout: post
title: "How to set up Eyelink 1000 and Presentation"
date: '2019-06-29'
author: Suhas Vijayakumar
tags:
- academia
- how to
---

This is a quick how-to post for setting up an experiment with Eyelink 1000 eye tracker and Presentation software.

*Special thanks to [Maarten van den Heuvel](https://www.mpi.nl/people/heuvel-maarten-van-den), at the Max Planck Institute, Nijmegen, who kindly sent me the scripts and the help guide which, will be available in a folder that you'll download in a minute.*

---

I recently collected data for an experiment in the scanner that used Eyelink 1000 eye tracker. I used Presentation software to present my stimulus and record participant responses. If you are planning to do something similar, you’ve come to the right pocket of the internet. First, download and extract a folder that has a help guide, and the necessary subroutines for Presentation [from here](https://my.pcloud.com/publink/show?code=XZbCk37ZsvRT8ivkqhkrdvUKpGazJHGvynCk).

**Note**: I work at the Donders Institute, so these notes are primarily written to run experiments here. If you’re somewhere else, I hope this will still be of some use to you.

## What do I need?
 - **This folder** - [download link](https://my.pcloud.com/publink/show?code=XZbCk37ZsvRT8ivkqhkrdvUKpGazJHGvynCk) <br> It's the same folder from above. Just reminding you to download it.
 - **PresLink**
 <br> This is an extension provided by SR Research’s team, and is already setup at DCCN's MRI lab. If you’re not at Donders, take a look at “Before you begin” section in the help guide (you’ll find it in the folder that you've downloaded under the name "**PresLink_help_file.pdf**").

 - **Knowledge of the port numbers linking your stimulus PC and Eyelink PC**
 <br> Your lab manager should have all the answers.

 - **Some subroutines that interact with Eyelink**
 <br> You'll find them in the folder that you just downloaded.

## So, how does this work?
For a simple experimental, which does not include manipulating stimulus based on gaze direction, or eye coordinates, or any data from Eyelink PC, the setup is quite straightforward. You only need to:
-	start recording eye tracker data
-	present stimulus and run experiment
-	stop recording eye tracker data

You’ll have to do the following:

1. **Add PresLink to Presentation.**
<br> This is already done at DCCN's MRI stimulus PC. But open your Presentation experiment, and check _Tools > Extension Manager_, which should have a registered PreLink extension.
<img src="/assets/blog/preslink/01_preslink_extension.png" class="image-responsive">

2. **Add output port to ensure Eyelink and stimulus PC can “talk”.**
<br> At the DCCN, output port that can send triggers from your stimulus PC to your Eyelink PC is COM port 2. Here are the settings that I used -
<img src="/assets/blog/preslink/02a_output_trigger_setup.png" class="image-responsive">
<img src="/assets/blog/preslink/02b_output_trigger_properties.png" class="image-responsive">

3. **Add eye tracker subroutines to your pcl file.**
<br> This is essentially one line in your pcl file. I called the file "proj_caudal_PFC_presentation_eyelink_SUBS.pcl" for my project. Feel free to call it however you see fit. A copy of the file is in the folder under the name "**EyelinkSUBS.pcl**": <br> `include "proj_caudal_PFC_presentation_eyelink_SUBS.pcl";`

4. **Define your output filename and initialise PresLink** <br> `Note:` There is an 8-character limitation on your EDF (that's the file extension Eyelink uses) filename. I used "sub_1", "sub_19" and so on. One line each.
<img src="/assets/blog/preslink/03_eyelink_start.png" class="image-responsive">

5. **Calibration and other details**
- I had issues getting Eyelink version automatically. So, I hardcoded it in the subroutines file.
<img src="/assets/blog/preslink/04_eye_tracker_version.png" class="image-responsive">
- I also experienced issues with getting screen sizes automatically.
<img src="/assets/blog/preslink/05_screen_HW.png" class="image-responsive">
- Did calibration using an external tool available on stimulus PC.

6. **Add lines to send output trigger for important events** (like beginning of a trail). <br> `Note:` At the DCCN, every button press (at least of the first two buttons, I've been told) is automatically sent to the eye tracker PC. So, choose a number that’s more than 2, when sending your trial-relevant trigger. <br> <br> So, start by defining your port:
<br> `output_port eye_tracker_port = output_port_manager.get_port(1);` <br> I only used 1 output port. If you're using multiple ports, enter the  correct number in the paranthesis. <br> <br> Then, add this line to send the trigger: <br> `output.send_code(4);` <br> Here, 4 was my code to denote the begining of a trial.

7. **Stop recording** - this will also export your eye tracking data to your desired location (default: logfile directory).
<img src="/assets/blog/preslink/06_eyelink_stop.png" class="image-responsive">

And that's about it! You should have a working eye-tracking setup with Eyelink 1000 and Presentation now. If anything is unclear, feel free to [send me a tweet](https://twitter.com/intent/tweet?text=Hi%20%40neuroacademic%2C%20Coffee?) or [an email](mailto:vijayakumar.suhas@gmail.com).
