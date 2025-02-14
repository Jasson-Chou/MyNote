**Version Number**  
Version: [Version number, e.g., 2.2.*] - Public  
Release Date: [yyyy-MM-dd] - OS Compatible Version 1.9 Ver  

**New Features**  
1. Added functionality to create Bin Table files.  
2. Added functionality to edit Bin Table files.  
3. Added import/export features for Bin Table files in CSV and Excel formats.  
4. Added functionality to create Bin Table template files.  
5. Added backup functionality for Bin Table (Save As for file selection).  
6. Added backup functionality for Bin Table (selecting from Backup Project).  
7. Implemented automatic Bin Table versioning. When transitioning to this version, users will be prompted whether to switch Flow Table to Bin Table editing. Selecting "Yes" automatically converts and selects the Bin Table file in SPJT; selecting "No" will continue using Flow Table for Bin distribution.  
8. When Bin Table options are closed in the current Solution, an "Upgrade Bin Table Version" function will appear in the Project Menu for user upgrades.  
9. Added version restrictions for importing Flow Table Excel files. If incompatible with the current Solution settings, an error message will appear.  
10. After creating a Template File, users will be prompted to open the folder containing the file.  
11. When upgrading file versions, version update messages are displayed in the Output panel.  
12. Added checks for AWG file PinName validation during builds.  
13. Added rules for DPS Gang checks.  
14. Added Release Note visibility on the Start Page and in Help -> Release History.  
15. Added Fatal Message display. Users are advised to contact AE if displayed.  
16. Added "Create Template File" option to the Start Page.  

**Improvements**  
1. Improved Pin selection in Pin Group operations for better user experience. After applying, users are prompted to delete undefined Pins; selecting "Yes" deletes them, while "No" retains user edits.  
2. Displayed all undefined Pin Names in the Pin Group during Project builds.  
3. Optimized program logic for file version updates.  
4. Resolved difficulty editing blocks in the SPJT editor when the screen size is too small.  
5. Added notifications for invalid characters during Rename input.  
6. Fixed failures when copying cell contents in Signal Slot definitions.  
7. Prevented users from creating new Solutions in the same location.  
8. Enhanced error message clarity during Timing Data builds.  
9. Optimized CPU usage for bulk cell edits (Paste, Import, Replace Text, etc.). Efficiency improved by ~98.57% to 99.44% during tests with 1000 Pins and 4–32 Sites.  
10. Improved user experience when selecting ComboBox options, eliminating the need for additional mouse clicks.  
11. Enhanced various user experience operations.  

**Bug Fixes**  
1. Fixed an issue where Import SPJT Procedure did not specify Solution version 2.1.  
2. Resolved errors when loading AWG files in projects.  
3. Fixed issues where OS version info in MAP scans might not list correctly.  
4. Corrected calculation errors in exported Signal Slot Excel file fields.  
5. Fixed inability to copy text in Signal Slot editing.  
6. Fixed errors in GUI location indicators during Timing Data builds.  
7. Addressed issues where renaming Solutions with identical names caused *.msln to disappear.  
8. Fixed Solution Project and Solution Name validation checks.  
9. Resolved issues where unsaved file symbols (*) failed to display in certain conditions.  
10. Fixed unsaved file symbols (*) not triggering when editing Rows or Sites in Pin and PinGroup pages.  
11. Corrected Flow Table "Until Pass Count" field to prevent values less than 0.  
12. Fixed issues where Up/Down Limit fields in Limit Table did not display after editing.  
13. Resolved issues where closing the editor via the close button (x) did not trigger a prompt.  
14. Fixed Search/Replace Text positioning functionality.  
15. Addressed various known issues.  

**Technical Updates**  
1. Updated the mapping relationship between Source Files (signal, flow, ...) and UI (Field Mapper), enabling easier future additions and deletions. (Versions after 2.2 support seamless downgrades, with 2.2 as the minimum version.)  

**Known Issues**  
1. In rare cases, Visual Studio builds may fail. (Manually open the generated Visual Studio project and check for failure reasons.)  
2. The edited status symbol may be triggered when opening the editor. (Resolved but under observation.)  
3. In the Signal screen, editing the Pin Setting Tab triggers the unsaved file symbol (*). (Users will be prompted to save previous edits when switching to the Signal tab.)  

**Future Plans**  
1. Continued maintenance of Flow Table Bin distribution, with plans to fully transition to Bin Table in a future 2.X version.  
2. Upgrade Telerik components and update .NET Framework 4.6.1 to a newer version in 2.X.  
3. Add Search/Replace Text targeting specific file groups (e.g., Flow Table files within the current Solution).  
