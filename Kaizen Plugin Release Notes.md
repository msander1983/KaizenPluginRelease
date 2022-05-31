# Release notes - Kaizen Plugin

## 2022-05-31 (2.2.3)
- The QuickWord/PDF/HTML doesn't support non-default output files or folders: added error message to tell you about it.

## 2022-02-26 (2.2.2)
- BUGFIX: A fix to the problem that caused the Quick PDF/Quick Word to sometimes fail in Flare 2021r3
- BUGFIX: A fix to the problem where condition export would not work in Flare 2021r3
- FEATURE: You can now build a "Quick HTML" target that'll build a CleanXHTML version of the topic you have open. 

## 2021-12-13 (2.2.1)
- Updated the Kaizenscript functionality so that you can re-install a script without deleting the existing DLL file first. 

## 2021-11-02 (2.2.0)
- The KaizenScript functionality was redesigned to allow for faster and easier deployment of custom add-ons to the Kaizen Plugin. 
	- **NOTE:** This means that existing Kaizen Scripts will no longer work. Please e-mail me at mattias@improvementsoft.com for a free conversion. 
- Bug fix: If you manually put in the MadCap prefix in the tag replacer destination field you would get an error message. No more! :) 

## 2021-10-20 (2.1.4)
- When opening a file from the TO DO notes function - the Link Viewer would not work. That has been corrected now.
- Removed the old Kaizen Script functionality.
- When importing Micro content from Excel, you can now include alternative terms by separating the entries with ";", e.g. Lorem;Ipsum.
- PDFs created by the Quick PDF feature now get a unique name with a time stamp to avoid conflicts in Adobe Acrobat. 
- Quick PDF is now more robust. 
- The condition tag export for files and targets now support condition tags with certain special characters, and includes conditions for targets with the default TOC set.

## 2021-08-03 (2.1.3)
- The fast file search normal search is now case insensitive. 

## 2021-07-23 (2.1.2)
- Bug fixes. 

## 2021-07-09 (2.1.1)
- Fixed a bug where replacing empty tags would result in a remaining `<REMOVEABC />` tag.
- Fixed a bug where target condition use export would not include the condition file name if it had a hyphen.

## 2021-05-11 (2.1.0)
- The release flow was optimized. 

## 2021-05-11 (2.0.7800.28098)
- The installer now has silent mode enabled (/S)

## 2021-04-26 (2.0.7786.20438) 
- Corrected bug related to creating a TOC and bookmarking the topic, as well as bug that would sometimes remove text when all changes were accepted. 

## 2021-04-09
- Added button to open a random topic or snippet

## 2021-03-17 (2.0.7746.14208) 
- Clarified MD1 vs MD2 icons.

## 2021-03-16 (2.0.7745.39186)
- Updated help call URL. 

## 2021-03-09 (2.0.7738.17309) 
- Fixed a bug that causes the topic creator functionality to crash in some cases. Added small icons to buttons. 

## 2021-03-06 (2.0.7735.36061)
- New color icons that work better for dark mode.              

## 2021-02-12 (2.0.7713.20478)
- Various changes for the release of the separate [docs.improvementsoft.com](https://docs.improvementsoft.com/Content/Documentation/Markdown II.htm). 

## 2020-12-18 (2.0.7657.23742)
- Corrected a bug, where  accepting all tracked changes in a project would skip files where the  `<MadCap:changeData>` element had attributes. 

## 2020-12-14 (2.0.7653.21440)
- Various bug fixes for the Markdown plugin. See [docs.improvementsoft.com](https://docs.improvementsoft.com/Content/Documentation/Markdown Plugin.htm).                                                                                                                            
- Fixed a bug that causeed the Sort TOC function to crash.                                                                                                                             
- You can now add TODO's to TOCs as well as topics and snippets.                                                                                                                             
- Fixed a bug that caused the Fast File Search function to miss files in the Project folder.                                                                                                                            
- The Validate XML function now supports all types of Flare files, not just topics and snippets. 

## 2020-10-14 (2.0.7592.23195)
- Bug fixes                                                                                                                                                
- Added config file to support differences in table import settings. 

## 2020-09-29 (2.0.7577.23994)
- Bug fixesThere was an issue with the Markdown plugin license key that prevented you from running the KaizenCommander CLI tool. 

## 2020-09-17 (2.0.7565.33411)
- Bug fixesMarkdown table with empty header elements would cause the import to fail. The **Apply Links to TOC** function no longer overwrites links to external http sources. 

## 2020-05-18 (1.0.7433.19185)
- Bug fixesTo Do notes form buttons no longer disappear when you resize the window. If a Markdown table had HTML code it would not be properly imported. 

## 2020-05-08 (1.0.7433.18756)
- Bug fixesAdvanced Tag Replacer fix.Markdown export fix.Tag replacer - nested tags - fix. 

## 2020-05-06 
- Advanced Tag Replacer. You can now search and replace tags with any attribute using free text  search or REGEX. Additionally - you can now also wrap a tag in another  tag using the Advanced Tag Replacer. 
- See [Replace tags using REGEX](https://docs.improvementsoft.com/Content/Documentation/Kaizen Plugin.htm#Replace).                                        
- Added an installation helper for KaizenScripts.                                         
- Added feature that converts the first sheet of an Excel file to a HTML table and puts the code on your clipboard.                                        
- You can now add a Google Calendar or Outlook reminder to review a specific topic from the **Productivity** tab.                                        
- Updated the installer to work for Flare 2020.                                        
- Bug fixes. 

## 2020-03-07 
- Micro content import from Excel. For instructions, see [Import micro content from Excel](https://docs.improvementsoft.com/Content/Documentation/Kaizen Plugin.htm#Import).                                        Bug fixes 

## 2019-09-20 (1.0.7202.23531)
- Bug fixes in relation to the updated Markdown plugin.        

## 2019-09-06 
- The Tag Replacer is now significantly faster to use in projects with a lot of files.                                         
- GUI changes                                         
- Setting alt image texts in batch                                        
- Statistics feature 

## 2019-07-31 
- Updates to the Markdown plugin.                                         
- Bug fixes. 

## 2019-05-31 
- Updated link to online help.                                         
- Internal improvements to the Quick PDF functionality. 

## 2019-04-18 
- Releasing updated Accept/Reject all changes-functionality.   
