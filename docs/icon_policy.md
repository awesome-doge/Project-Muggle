# Icon policy
This document provides guidelines for contributing icons used in the Bitcoin Core GUI.

 

## Preparing Contribution
Both an icon source file, in Scalable Vector Graphics (SVG) format, and an optimised production file, in Portable Network Graphics (PNG) format, are required for 
each icon.

SVGs are used as source files due to being able to scale to any size whilst retaining image quality, but are not used in production due to limited support by 
applications. If different sized production (PNG) icons are required they can be generated from the associated scaled SVG source file in a vector based tool like 
Inkspace, Adobe illustrator, Figma, Sketch or Adobe XD.

PNGs are used in production due to their wide support in applications, support of transparent backgrounds and better image quality than competing file types 
such as JPEG.

### Icon Style
Icon style should follow a few basic principles to maintain consistency and clarity:

- Icons should be minimal with little to no fine details. 
- Icon shapes should be consistent and avoid organic elements that do not scale well.
- Icon colors should be consistent with other icons used in Bitcoin Core. 
- Icons should should fit within the 'live area' of the icon grid - see below.

### Icon Grid
Bitcoin Core's icon set uses an 8-point grid system which utilises size increments of 8 (in pixels) to visually orientate elements within a grid. An even
number like 8 to position icon elements makes scaling on a wide variety of devices easy and consistent. Most popular screen sizes are divisible by 8 which makes 
fitting elements easier with an 8-point grid system. Overall, this makes things more efficient for designers and maintains consistency across applications.


### Optimizing Production Files (PNG): 
Production (PNG) files are to be optmized before being added to Bitcoin Core. Optimizing PNG files removes various color profiles, ancillary (alla) and text chunks resulting in a reduction in size of the image file losslessly (without a lowered image quality). Various PNG optimizers exist, below are some examples:

- Open source tool [ImageOptim](https://imageoptim.com/api).
- Open source tool [Trimage](https://trimage.org/).
- (Advanced) Run them through Bitcoin Cores [optimize-png.py](https://github.com/bitcoin-core/bitcoin-maintainer-tools/blob/master/optimise-pngs.py) script.



## Contributing
Icons should only be added via pull request (PR) in two situations:

- An icon used in production is being replaced with a new icon.
- A new feature is being added to the Bitcoin Core GUI that requires the addition of a new icon.

Icons (both SVG and PNG) should not be added to the repo if they are not yet used in production. If a new icon is set to be added in an upcoming PR the designer of the icon should [open an issue](https://github.com/bitcoin-core/gui/issues/new/choose) to get feedback on the design of the icon and to make sure the design is
consistent with Bitcoin Core's iconography.  

#### Source files (SVG)
Source SVG files should be added to `src/qt/res/src` at 24x24px.

#### Production files (PNG)
Optimized production PNG files should be added to `src/qt/res/icons` at 24x24px.



## Attribution 
Icon additions should have the appropriate attribution to the author, the licence used for the icon and any comments relevant to the icon included in the 
[contrib/debian/copyright](https://github.com/bitcoin-core/gui/blob/master/contrib/debian/copyright) file.