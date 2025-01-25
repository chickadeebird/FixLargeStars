# FixLargeStars

This is a Pixinsight script that takes larger stars and "fixes" abnormal surrounding artifacts. This could include uneven coloration or an abnormal shape. It takes the top specified percentage of stars detected within a starfield, based on star intensity, and replaces the stars with ideal shapes.

The Fix Large Stars tab uses the star detector settings in the accompanying Star Detector Settings tab.

Fix Large Stars works by taking the top specified percentage of stars based on intensity and replacing them with idealized new stars. These idealized new stars are replicated based on the PSF characteristics of the original star including the RGB intensity, widths of the Moffat axes, etc.

The "Top percentage of stars to replace" slider specifies the percentage of bright stars to replaced ranked based on intensity, ie the top X% of stars will be analyzed and replaced. Higher values means more stars will be replaced. 4 might be a good place to start.

The "Maximum star size slider" limits the maximum size of a star to replace in total number of pixels (the area of the star plus the associated anomaly). Setting this to a high value includes all structures, and a low value exludes larger structures from being repaired.

# Usage

The algorithm should work on mono and multi-channel/RGB images. It should also work on linear and nonlinear data.

## Images

This is a linear RGB image stack with an artifact seen with the larger, brighter stars. The image on the left is the original image and the image on the right is the "fixed" image.

<img src="./figs/FixLargeStars fixed stars.png" text='FixLargeStars script' align=left />

## Script

This is the script interface for the FixLargeStars script.

<img src="./figs/FixLargeStars script.png" text='FixLargeStars script' align=left />

This can be found here: ChickadeeScripts > FixLargeStars after installation.

## Manage repository location

In order to automatically install and subsequently refresh script updates in Pixinsight, add the following URL to Resources > Updates > Manage repositories

https://raw.githubusercontent.com/chickadeebird/FixLargeStars/main/

After this has been added to the repositories, Resources > Updates > Check for updates should place the new FixLargeStars script in Scripts > ChickadeeScripts

