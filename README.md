# photo-scripts

A set of useful scripts for photo processing.

## Installation

    $ ./install

## ps-build-hdr

Build HDR-photos from a set of photos

#### Synopsis
    ps-build-hdr -n|--number NUMBER
    ps-build-hdr -h|--help|--usage
    ps-build-hdr [FILENAME]...

#### Description
Build HDR-photos from the photos in current directory by NUMBER photos
in each set. It is supposed that current directory contains photos only
and in each set there is the same photo is presented but made with
different exposures. The processing is based on the
[article of Dr.Lex](https://www.dr-lex.be/info-stuff/luminancehdr.html) and automated.
The default number in each set is 3 as it is a usual bracketing number
for most cameras. It is also possible to process not the whole
directory but any number of given photos.

#### Parameters
|Parameter|Description|
|---------|-----------|
|-n NUMBER, --number NUMBER | A number of photos is each set (default 3) |
|-h, --help, --usage        | Display this information and quit |
|FILENAME                   | A set of photo filenames |

#### Examples
        ps_build-hdr
               Build HDR-photos from the current directory by 3 in a set.

        ps-buld-hdr --number 5
               Build HDR-photos from the current directory by 5 in a set.

        ps-buld-hdr photo1.jpg photo2.jpg ../photo3.jpg
               Build an HDR-photo from 3 provided photos.
