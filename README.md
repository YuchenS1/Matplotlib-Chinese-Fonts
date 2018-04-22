# Matplotlib-Chinese-Fonts
Easy way to fix Chinese character display issues in matplotlib

________________

*This is only tested on macOS Sierra.*

*fontList.json should not be downloaded and used to replace similar local files on your computer, because many settings in fontList.json is specific to my computer.*

*fontList.json is only uploaded to be used as a reference when editing your own.*

________________


1. Download 'matplotlibrc' and replace the same one on your computer somewhere in /usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/
2. Locate 'fonts' folder in /usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/fonts/
3. You should see three folders: 'afm', 'pdfcorefonts', 'ttf'.
4. Open 'ttf'.
5. Drag and drop your chosen Chinese font (.ttf) into ttf folder.
    Note: you can download .ttf font files anywhere online.
6. Locate 'fontList.json' in /users/[Your User Name]/.matplotlib/fontList.json
7. Open 'fontList.json'
    
    Look something like this:
    {
  "_version": 201,
  "_FontManager__default_weight": "normal",
  "default_size": null,
  "ttffiles": [
    "/usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/fonts/ttf/DejaVuSansMono-Oblique.ttf",
    "/usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/fonts/ttf/STIXGeneralBol.ttf",
    "/usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/fonts/ttf/STIXNonUni.ttf",
    "/usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/fonts/ttf/STIXSizThreeSymBol.ttf",
    "/usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/fonts/ttf/cmss10.ttf",
    "/usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/fonts/ttf/STIXSizFiveSymReg.ttf",
    "/usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/fonts/ttf/cmex10.ttf",
    "/usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/fonts/ttf/STIXGeneral.ttf",
    "/usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/fonts/ttf/DejaVuSansMono-Bold.ttf",
    "/usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/fonts/ttf/DejaVuSans-Oblique.ttf",
    "/usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/fonts/ttf/cmmi10.ttf",
    "/usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/fonts/ttf/DejaVuSerifDisplay.ttf",
    "/usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/fonts/ttf/DejaVuSerif.ttf",
    "/usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/fonts/ttf/STIXSizOneSymReg.ttf",
    ......
    ]


8. Add the path to your added .ttf file in between any of these file paths.
9. Scroll down until you find something like this:
      
    
  "defaultFamily": {
    "ttf": "SimHei",
    "afm": "Helvetica"
  },
  "defaultFont": {
    "ttf": "/usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/fonts/ttf/SimHei.ttf",
    "afm": "/usr/local/lib/python3.6/site-packages/matplotlib/mpl-data/fonts/afm/phvl8a.afm"
    
10. Change defaultFamily {'ttf'} to your Chinese font name
11. Change defaultFont {'ttf'} to the path that leads to your Chinese font .ttf file

