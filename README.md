# ht-autocondition

An autohotkey macro for autmating high tension (HT) conditioning for Tecnai 12 electron microscoptes.

TEMs can be finicky about jumping HT from zero to hero.  It can be healthier to incrementally raise the HT - but it's a laborious waste of time.  This script can be used to automate this process so both you and your microscope can live long and prosper.


## How to use it

 1. Install [AutoHotKey](https://www.autohotkey.com/) on your microscope computer.  (For 32-bit Windows XP systems, AHKv2 is the last 32-bit compatible version).
 2. Add AutoHotKey.exe to your Windows path.
 3. Run the provided ht_routine_on.txt script using the following command in terminal.  (You may need to run the terminal window as an adminstrator.)

`AutoHotkey.exe ht_routine_on.txt`

 4. Turn on your microscope high tension at 40 kV.  Select the "Free High Tension" tickbox.
 5. Click to select the High Tension window within the TEM user interface.
 6. Press `Ctrl+J` to start the routine.
 7. HT will increase slowly up to 120 kV.  The total routine will take 4 h 15 min to run to completion.  During the run, check in on the microscope every 30-60 min to ensure that column vacuum is stable and to top up liquid nitrogen in the finger dewar.
 8. After the routine has finished, disable it by killing the autohotkey process in Process Manager (accessible in Windows by pressing `Ctrl+Shift+Esc`).


## Conditioning Routine

 1. Increase by 3 kV every ~5 min from 40 kV to 100 kV
 2. Increase by 1 kV every ~5 min from 100 kV to 110 kV
 3. Increase by 1 kV every ~10 min from 110 kV to 120 kV


## Troubleshooting

 - The mouse positions for clicking are hardcoded and may need to be adjusted for different screen resolutions.  We recommend doing a test run with the high tension off in software to ensure that the script clicks where you expect it to.  If not, you may need to manually adjust the click positions.
 - Running an automatic process on your microscope carries an element of risk.  We disclaim any liability for any damage to equipment that running this script causes.  Please be careful, and make sure you verify that the script is behaving as you intend it to!
 - Feel free to open an issue in GitHub if you encounter any problems and I'll do my best to help out.  Cheers!

> Written with [StackEdit](https://stackedit.io/).
