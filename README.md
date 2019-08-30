## DownloadMyThings

The purpose of this tool is to enable the bulk download of all my Things I've posted on Thingiverse.  I can recapture photos, models, tags and descriptions of Things that I haven't saved locally.  Given this information I can do a variety of things such as:

* Keep a local copy of my Things
* Upload my designs to other sites
* Close my Thingiverse account without losing my own IP

## Instructions

Given that this tool runs locally on your system, using an App Token works fine.

1. Create an App at https://www.thingiverse.com/developers/my-apps

   I called mine "Download My Things"  
   Platform: Desktop  
   Leave your app unpublished  
   After creating, note your **App Token** which you need.

2. Update your local config file with the issued App Token.

   **Note the App Token is a read-only secret and you probably don't want to share it**

3. Run the tool!

```
$ ./dlthings -h
usage: dlthings [-h] [-u USER] [-o [OUTDIR]]

optional arguments:
  -h, --help            show this help message and exit
  -u USER, --user USER  Thingiverse user whose Things you're downloading
  -o [OUTDIR], --outdir [OUTDIR]
                        DIRECTORY to download things into
```

## Example

```
$ ./dlthings -u mikeymakesit -o /Volumes/home/3D\ Printing/MyThings
Downloading Things to: /Volumes/home/3D Printing/MyThings
3831190
Wrote Thing metadata
~> /Volumes/home/3D Printing/MyThings/3831190/files/StarSplash-.6high-6x6.stl
Downloaded 0 objects for Thing 3831190
~> /Volumes/home/3D Printing/MyThings/3831190/photos/IMG_0857.jpeg
Downloaded 0 photos for Thing 3831190
3831194
Wrote Thing metadata
~> /Volumes/home/3D Printing/MyThings/3831194/files/Plaid-Thick-.6high-6x6.stl
~> /Volumes/home/3D Printing/MyThings/3831194/files/Plaid-Thin-.6high-6x6.stl
Downloaded 0 objects for Thing 3831194
~> /Volumes/home/3D Printing/MyThings/3831194/photos/IMG_0858.jpeg
~> /Volumes/home/3D Printing/MyThings/3831194/photos/IMG_0860.jpeg
Downloaded 0 photos for Thing 3831194
2906890
Wrote Thing metadata
+> /Volumes/home/3D Printing/MyThings/2906890/files/AAx7-Right.stl
+> /Volumes/home/3D Printing/MyThings/2906890/files/AAx7-Left.stl
Downloaded 2 objects for Thing 2906890
+> /Volumes/home/3D Printing/MyThings/2906890/photos/IMG_0255.jpg
+> /Volumes/home/3D Printing/MyThings/2906890/photos/421c7ec582ae87588d75638676c1ac44.png
+> /Volumes/home/3D Printing/MyThings/2906890/photos/a114e9408e0ea96e12470b64c90c8b5f.png
+> /Volumes/home/3D Printing/MyThings/2906890/photos/IMG_0254.jpg
Downloaded 4 photos for Thing 2906890
Done!
```

## Notes

When you see "~>" it means the object/photo already exists on your system and was not downloaded again.  
Example of files already downloaded:

```
~> /Volumes/home/3D Printing/MyThings/3810982/files/HeadphonesHanger1.stl
~> /Volumes/home/3D Printing/MyThings/3810982/files/HeadphonesHanger2.stl
Downloaded 0 objects for Thing 3810982
```

When you see "+>" it means the object/file was downloaded successfully.  
Example of new files just downloaded:

```
+> /Volumes/home/3D Printing/MyThings/3081067/files/Top-MMU-8.stl
+> /Volumes/home/3D Printing/MyThings/3081067/files/Top-MMU-3.stl
+> /Volumes/home/3D Printing/MyThings/3081067/files/Top-MMU-4.stl
+> /Volumes/home/3D Printing/MyThings/3081067/files/Top-MMU-6.stl
+> /Volumes/home/3D Printing/MyThings/3081067/files/Top-MMU-5.stl
+> /Volumes/home/3D Printing/MyThings/3081067/files/Top-MMU-9.stl
+> /Volumes/home/3D Printing/MyThings/3081067/files/Top-MMU-7.stl
+> /Volumes/home/3D Printing/MyThings/3081067/files/Top-MMU-2.stl
+> /Volumes/home/3D Printing/MyThings/3081067/files/Bottom.stl
+> /Volumes/home/3D Printing/MyThings/3081067/files/Top-MMU-1.stl
+> /Volumes/home/3D Printing/MyThings/3081067/files/Top.stl
Downloaded 11 objects for Thing 3081067
```

