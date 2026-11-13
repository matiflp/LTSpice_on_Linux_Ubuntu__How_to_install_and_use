# LTspice on Linux Ubuntu - How to install and use
Make great analog designs

## Description
This are the steps to install and use LTspice 64 bits on Linux Ubuntu 20.04 . <br>

## Installation

```bash
# Update your package manager
sudo apt update

# Install Wine
# Note: Starting from Ubuntu 24.04 (Noble Numbat), the package 'wine-stable' was replaced by 'wine' in the official repositories.
# For Ubuntu 24.04 and newer:
sudo apt install wine

# (For older versions like Ubuntu 20.04 / 22.04, you can still use: sudo apt install wine-stable)

# Download LTspice 64 bits
cd /tmp/
wget https://analog.com

# Install LTspice
wine LTspice64.exe
rm LTspice64.exe
```

## How to execute LTspice 

```
# Start lstpice through wine
wine ~/.wine/drive_c/Program\ Files/LTC/LTspiceXVII/XVIIx64.exe
```

## Create a directory for your simulation files

```
# To open file in LTspice, move it to somewhere in ~/.wine/drive_c folder which is the C drive in wine.
mkdir ~/.wine/drive_c/Program\ Files/LTC/LTspiceXVII/examples/Educational/my_ltspice_files

# Copy file from Examples to my_ltspice_files diretory this is more pratical.
cp ~/.wine/drive_c/Program\ Files/LTC/LTspiceXVII/examples/Educational/Clapp.asc ~/.wine/drive_c/Program\ Files/LTC/LTspiceXVII/examples/Educational/my_ltspice_files/Clapp.asc 

# In this way it is better organized but the examples are far away from your projects directory.
mkdir ~/.wine/drive_c/my_ltspice_files_2
cp ~/my_files/test.asc ~/.wine/drive_c/my_ltspice_files_2/
```

## Fix Small Fonts / High-DPI Scaling

By default, Wine uses a 96 DPI screen resolution, which makes menus and text in LTspice look very small on modern Full HD or 4K monitors. To fix this:

1. Open your terminal and run the Wine configuration tool:
   ```bash
   winecfg
   ```
2. Go to the **Graphics** tab at the top.
3. Under **Screen resolution**, move the slider from `96 dpi` to **144 dpi** or **192 dpi** (depending on your screen size).
4. Click **Apply**, then **OK**, and restart LTspice.

## LTspice Help Manual

The help file ```LTspiceHelp.chm``` will not open correctly inside LTspice. But LTspice, comes also with the documentation in the PDF format. The file is ```LTspiceHelp.pdf``` , just open it.

To open the file ```LTspiceHelp.pdf``` just do:

1. Open the file explorer on Linux ```/home/<user>/``` .

2. Do **Ctrl + H** to see the hidden files and directories that start with a "." (dot) .

3. Navegate to ```~/.wine/drive_c/Program Files/LTC/LTspiceXVII/```

4. Double click on the file ```LTspiceHelp.pdf``` .

5. Do **Ctrl + H** to change again to not see the hidden files and directories that start with a "." (dot) .


## References on LTspice Simulation

1. **LTspice - Site Analog Devices** <br>
   Program, documentation, tutorials, videos. <br>
   [https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html](https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html) 

2. Play List - **LTspice tutorial** - **FesZ Electronics** <br>
   Great youtube Channel on LTSpice and Analog Design. <br>
   [https://www.youtube.com/playlist?list=PLT84nve2j1g_wgGcm0Bv3K4RSl2Jdjsey](https://www.youtube.com/playlist?list=PLT84nve2j1g_wgGcm0Bv3K4RSl2Jdjsey)

3. Play List - **LTspice** - **Getting Started Tutorial** - Official tutorials <br>
   [https://www.analog.com/en/education/education-library/videos/video-series/ltspice-getting-started-tutorial.html](https://www.analog.com/en/education/education-library/videos/video-series/ltspice-getting-started-tutorial.html) 

4. Play List - **LTspice** - **Essentials Tutorial** - Official tutorials <br>
   [https://www.analog.com/en/education/education-library/videos/video-series/ltspice-essentials-tutorial.html](https://www.analog.com/en/education/education-library/videos/video-series/ltspice-essentials-tutorial.html)

5. Video - **LTspice** - **Stepping Parameters** <br>
   [https://www.analog.com/en/education/education-library/videos/5579239884001.html](https://www.analog.com/en/education/education-library/videos/5579239884001.html)

6. Book - **The LTSpice XVII simulator** - Commands and Applications <br>
   by Gilles Brocard <br>

7. Book - **The LTSpice IV Simulator** - Manual, methods and applications <br>
   by Gilles Brocard <br>

## Have fun!
