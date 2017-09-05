Mogrify commands are usually in the following formats

magick.exe mogrify -path "/output\file/path" -format pdf -quality 100 *.TIFF

  the "pdf" in -format is obviously the output, and can be changed to what you like
    the -limit memory and -limit map is to allow me to use my max memory size, these are optional
      -quality 100 specifies I want 100% of the quality of the original in the final during the conversion
      -compress fax specifies I want the binaries of the original compressed during the conversion to save space, this is documented on the imagemagick website.
        *.TIFF is the input, i.e. * is the wildcard for the original file name, the output file will have the same name. TIFF is the file extension that you want mogrify to look for and convert, you can specify multiple by putting a list in brackets
        i.e. *.[TIFF,tiff,TIF,tif]
        
In order for mogrify to work on large folders of items (that you want converted) you need to change your directory to that of the items to convert, if you want to keep the originals (mogrify overwrites the originals if no output dir is specified) you need to create that directory within the same drive as the input.

i.e.

I have a massive folder of .TIFF files I want to turn into PDFs, some are multi-page while others are single page.
they reside in "V:\TEST". My output will be "./PDFs" (i.e. V:\TEST\PDFs). You may need to play with yours if you want it elsewhere.

in order for ImageMagick to do the heavy lifting, I need to do the following
1. open CMD
2. CD /D V:\TEST\ (change my working dir to that of my inputs)
3. C:\PATH_TO_ImageMagick_Store\magick.exe mogrify -path "./PDFs/" -format pdf -limit memory 0 -limit map 0 -quality 100 -compress fax *.TIFF
