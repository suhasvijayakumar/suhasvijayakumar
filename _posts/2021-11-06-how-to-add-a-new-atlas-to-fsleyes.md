---
layout: post
title: "How to add a new atlas to FSLeyes"
date: '2021-11-06'
author: Suhas Vijayakumar
tags:
- academia
- how-to
---

The neuroimaging data viewer software [FSLeyes](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FSLeyes){:target="_blank"} is equipped with a few atlases -- Harvard-Oxford Cortical Structural Atlas, Juelich Histological Atlas, MNI Structural Atlas, and the likes. It also allows its users to load and use custom atlases. Here's a brief how-to post about how to add a new atlas to FSLeyes.

We will use the Johnson et al., 2019 Canine Brain atlas as an example. If you would like to know more about the atlas and how it was made, please refer to the original open access publication \"Stereotactic Cortical Atlas of the Domestic Canine Brain\" at [this link](https://doi.org/10.1038/s41598-020-61665-0){:target="_blank"}.

## Steps to add a new atlas to FSLeyes

### step 1
Download the Canine brain atlas from [this link](https://ecommons.cornell.edu/handle/1813/67018.2){:target="_blank"}.

### step 2
Assuming you have downloaded it to the default Downloads folder, path to your Canine atlas will be `~/Downloads/Johnson_etal_2019_Canine_Atlas_v2`. Notice that the folder is equipped with a few files. The ones relevant for us are:

- `Canine-labels-update.xml`: the file that FSLeyes reads
- `Canine_population_template.nii.gz`: a template brain to visualise this 		atlas
- `whole_atlas_cortical_subcortical.nii.gz`: allows you to visualise various cortical and subcortical regions

### step 3
Open FSLeyes. If you are using the default layout, the screen should look like this

<img src="/assets/blog/fsleyes_add_atlas/01_fsleyes_default.png" class="image-responsive">

### step 4
Click on File > Import new atlas
<img src="/assets/blog/fsleyes_add_atlas/02_fsleyes_import_new_atlas.png" class="image-responsive">

### step 5
Navigate to the atlas folder, select `Canine-labels-update.xml` file, and click open. Surprisingly, there is no pop-up message that tells you if everything went well, as expected or if there was an error!
<img src="/assets/blog/fsleyes_add_atlas/03_fsleyes_select_atlas_file.png" class="image-responsive">


### step 6
Display your atlases by clicking Settings > Ortho View 1 > Atlases.
(shortcut: Cmd + Opt + 6).
<img src="/assets/blog/fsleyes_add_atlas/04_fsleyes_show_atlases.png" class="image-responsive">

### step 7
You should now see a section with all of the available atlases.
<img src="/assets/blog/fsleyes_add_atlas/05_fsleyes_display_atlases.png" class="image-responsive">

### step 8
Now, load the `Canine_population_template.nii.gz` file, either by dragging and dropping it on to the app, or File > Add from file
(shortcut: Cmd + O).
<img src="/assets/blog/fsleyes_add_atlas/06_fsleyes_load_template_brain.png" class="image-responsive">

### step 9
Unselect unwanted atlases, and select Canine 30N-Johnson-Barry-Atlas-Labels Update.

### step 10
If you now click on a brain region that is listed in the atlas, you should see its label.
<img src="/assets/blog/fsleyes_add_atlas/07_fsleyes_select_canine_brain.png" class="image-responsive">

### step 11
Clicking on \"Show/Hide\" option next to the atlas name allows you to visualise various brain regions in different colours.
<img src="/assets/blog/fsleyes_add_atlas/08_fsleyes_click_brain_region.png" class="image-responsive">

> Not all of the labeled regions are visualised in this way for some reason. `¯\_(ツ)_/¯` <br> So, let us make use of the `whole_atlas_cortical_subcortical.nii.gz` file.

### step 12
Load `whole_atlas_cortical_subcortical.nii.gz`, the same way you loaded the template brain (shortcut: Cmd + O).

<img src="/assets/blog/fsleyes_add_atlas/09_fsleyes_load_atlas_brain.png" class="image-responsive">

### step 13
Change colourmap of this file. I recommend using Random or one of the MGH ones.

<img src="/assets/blog/fsleyes_add_atlas/10_fsleyes_change_colourmap.png" class="image-responsive">

### step 14
This should make it easier to navigate between various regions and visualise their boundaries better.


<img src="/assets/blog/fsleyes_add_atlas/11_fsleyes_use_atlas.png" class="image-responsive">

### step 15
There is no step 15. Hope everything has worked out. Have fun!

Kindly excuse typos. If anything is unclear, or if you identify an error in this post, feel free to [send me a tweet](https://twitter.com/intent/tweet?text=Hey%20%40neuroacademic%2C%20){:target="_blank"} or [an email](mailto:vijayakumar.suhas@gmail.com).
