fusecam
=======

perl script for renaming images from digital cameras to a unified naming convention. 
Fuse is used to mount a virtual drive which contains links to all images in the scanned directories. 

### Naming convention is:

   IMG[Y][M][D][H][\dd]{0-4}[Mk][Iso][Flash]

> [Y],[M],[D],[H] are year, month, day and hour of image creation as one letter 0..9,'A'..'Z' (like hex but longer)
> 
> [\dd]{0-4} is the actual image number from the actual filename (but only up to 4 digits counting from the end)
> 
> [Mk] is a letter describing the Camera (defined by exif Make & Model and needs to be set in hash in perl script (-; =
> 
> [Iso] is one letter for Iso/100 (0..9,'A'..'G') or int(Iso/100) for Iso>1600
> 
> [Flash] 'F' is flash has fired

uses exiftool.


