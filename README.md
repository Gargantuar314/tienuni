# My personal package

This is my personal package/preamble `tienuni.sty` for most of my LaTeX files in university (hence `tien-uni`).

The file is a work in progress, bits and pieces collected from manuals and <tex.stackexchange.com>. Also it is really messy and really needs a clean-up, in terms of style as well as structure.

## How to use this file

I will lay out how I install my style file with MikTeX on Windows 10. For more details at least for MikTeX, see
+ <https://miktex.org/faq/local-additions>,
+ <https://miktex.org/kb/texmf-roots>.

1. Create a new directory which MikTeX should manage. This can be anything and practically anywhere. I use
   ```powershell
   C:\Users\{yourusername}\AppData\Local\localtexmf
   ```
   where `localtexmf` is the name I use (anything is okay). To adhere to the [*TeX Directory Structure*](https://miktex.org/kb/tds), create the directory
   ```powershell
   .\tex\latex
   ```
   
   To do this all in one swoop and also change directory, do in Powershell
   ```powershell
   $texmf = "$env:LOCALAPPDATA\localtexmf\tex\latex"
   mkdir $texmf
   ```
2. Add this directory to the "TEXMF root directories".

   Start MikTeX as an administrator. Go to
   ```
   Settings > Directories
   ```
   and go on the "plus" symbol to select the newly created directory.
3. Copy `tienuni.sty` to the current working directory.

   Probably the easiest way would be to download the file and move it to `.\tienuni\` or equivalently `$texmf\tienuni\`.

   Another way would be to just `git clone`:
   ```powershell
   git clone https:\\github.com\Gargantuar314\tienuni.git $texmf
   ```
4. In any of your LaTeX files, include `\usepackage{tienuni}` with the various (undocumented) options. Sadly, some of the are required 😬 (*Eek!*).