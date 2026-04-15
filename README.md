# Release Notes

- **Version 2.2.45** (2026-04-15)
  - Added Snippet Picker: search and insert snippets by name or content with live preview, Launchy-style keyboard navigation (type to search, arrow keys to browse, Enter to insert)
  - Added Variable Picker: separate ribbon button to search and insert variables by name or value
  - Snippets and variables now insert at the actual cursor position within text, splitting the text node correctly
  - Empty elements are replaced when inserting a block snippet or inline content into them
  - Inserting snippets and variables no longer causes the topic to close and reopen
  - Custom Block/Inline dialog when inserting single-block snippets, with clear button labels

- **Version 2.2.44** (2026-04-02)
  - Fixed false error reports caused by Flare internal exceptions (ObjectDisposedException on CatapultFlareFullDependencyMdiEditor) reaching the AppDomain handler, which lacked the Flare exception filtering already present on the UI thread handler

- **Version 2.2.43** (2026-03-25)
  - Fixed Data Import (Excel) becoming unresponsive when the file name pattern contains multiple placeholders (e.g., `[[ID]] [[Guideline]].flsnp`)

- **Version 2.2.42** (2026-03-25)
  - Fixed QuickWord/QuickPDF/QuickHTML TFS checkout crash by bypassing TFS checkout for plugin temp files (KaizenTempToc, KaizenTargets) and directly clearing the read-only attribute instead
  - Fixed MissingMethodException (`Url..ctor(String)`) on older Flare versions by using cross-version compatible `Url.ReplaceSource` API

- **Version 2.2.41** (2026-03-24)
  - Fixed QuickWord/QuickPDF/QuickHTML crash when checking out files from TFS source control, caused by an invalid leading backslash in the file path passed to the TFS provider

- **Version 2.2.40** (2026-03-09)
  - Fixed crash (AggregateException) during XML validation caused by a threading race condition when updating the progress dialog
  - Validation progress updates are now guarded against form disposal, preventing unhandled exceptions when validation completes quickly

- **Version 2.2.39** (2026-02-25)
  - Fixed Sort TOC to handle namespace-aware XML when resolving linked titles from topic files
  - Fixed Sort TOC crash when TOC entries have null or empty titles
  - Improved path handling in Sort TOC using Path.Combine instead of string concatenation
  - Sort TOC now gracefully falls back to filename when topic files cannot be loaded

- **Version 2.2.38** (2026-01-27)
  - Enhanced To Do Notes with configurable keyword filtering (TODO, FIXME, NOTE, REVIEW, HACK, and custom keywords)
  - To Do Notes now shows the annotated text and surrounding context for each item
  - Added source filtering to include/exclude TOC entries from To Do list
  - Added search functionality and keyword color-coding to To Do Notes
  - Settings are now saved per-user and restored when reopening the form

- **Version 2.2.37** (2026-01-27)
  - Added new "Excel to Auto Suggestions" feature on the Import tab that converts an Excel file to a Flare Auto Suggestions file (.fltbx)
  - Simply create an Excel file with phrases/sentences in the first column and import them as auto suggestions for faster content authoring

- **Version 2.2.36** (2026-01-20)
  - Fixed exception filtering for non-English Windows installations where localized stack traces use translated keywords (e.g., "ved" in Norwegian instead of "at").

- **Version 2.2.35** (2025-12-12)
  - Fixed B3.* exception filtering to check TargetSite namespace when StackTrace is not yet populated.

- **Version 2.2.34** (2025-11-24)
  - Enhanced error filtering to ignore all MadCap Flare internal exceptions (B3.* namespace) instead of only specific B3 libraries.

- **Version 2.2.33** (2025-11-07)
  - Misc bug fixes related to error catching. 

- **Version 2.2.32** 
  - Misc bug fixes.

- **Version 2.2.31** (2025-10-20)
  - Added new "Snippet Usage Report" feature that analyzes all snippets in a project
  - Report shows usage count for each snippet with sortable columns
  - Includes progress dialog with real-time updates and cancellation support
  - Optimized performance: reads each file only once instead of once per snippet (up to 500x faster for large projects)
  - Smart double-click behavior: opens all files for multi-use snippets with user confirmation
  - Helps identify unused or rarely-used snippets for cleanup and maintenance

- **Version 2.2.30** (2025-10-15)
  - Fixed QuickWord timing bug where builds succeeded but files older than 20 seconds were rejected - increased threshold to 60 seconds and added detailed diagnostics
  - Plugin now filters out Flare's internal B3 library errors, passing them to Flare's error handling instead of showing KaizenPlugin error reports
  - Improved error messages when output files are found but too old, with suggestions to delete output folder

- **Version 2.2.29** (2025-10-10)
  - Apply Links to TOC now excludes PDFs, preserving manually entered PDF titles instead of overwriting them with filenames
  - Fixed QuickWord to properly find .docx files (pattern changed from *.doc to *.doc*)
  - Fixed misleading error messages - now says "Try closing the output file" instead of "PDF" for all document types
  - Fixed log parser to extract any file type from build logs, not just PDFs
  - Error reports now include last 10 lines from MadCap build log (.mclog) for better diagnostics

- **Version 2.2.28** (2025-10-04)
  - Added new Settings feature allowing users to customize which groups are visible within each tab
  - QuickPDF, Quick Word, and Quick HTML now work for snippets. 

- **Version 2.2.27** (2025-09-25)
  - Quick PDF and Quick Word and Tag Replacer, and Accept/Reject All Changes now works with Flare 2025 r2
  - Better error logging

- **Version 2.2.26** (2025-08-26)
  - Fixed Advanced Tag Replacer form appearing as topmost window by explicitly setting TopMost property to false
  - This ensures the form doesn't stay on top of other windows during use

- **Version 2.2.25** (2025-08-05)
  - Fixed ZIP backup compatibility with Windows Explorer by implementing a new manifest-based format while maintaining backward compatibility with legacy ZIP files
  - Added user-friendly read-only file handling during restoration
  - Fixed "Out of Memory" error when processing SVG files in the Set Alt Text dialog
  - Added proper error handling and UI improvements for better user experience
  - Added "Export Glossary to Excel" feature that extracts glossary terms, definitions, and links from .flglo files into Excel spreadsheets
  - Added enhanced XML validation options allowing users to validate XML for specific folders, TOC files, individual topics, or the entire project, with improved TOC relative path resolution

- **Version 2.2.21-24** (2025-05-23)
  - Misc bug fixes, and an update to the installer

- **Version 2.2.20** (2024-02-21)
  - Fixed a bug related to Data Import, where if the file name field had a "/" - the imported file would only contain the part after the slash

- **Version 2.2.19** (2023-12-11)
  - Fixed a bug related to Micro Content Import

- **Version 2.2.15** (2023-09-26)
  - Improved memory management in the ALT texts feature

- **Version 2.2.14** (2023-07-31)
  - Fixed bug in Tag Replacer
  - You can now validate XML in specific folders
  - Various bug fixes

- **Version 2.2.13** (2023-06-21)
  - Support for multiple file extensions in the Fast File Search
  - New button to close all topics and snippets

- **Version 2.2.12** (2023-06-14)
  - When accepting all changes in a project, non-significant line breaks would be removed. Now they are not

- **Version 2.2.11** (2023-05-30)
  - Fixed a bug where the tabs would duplicate in Flare
  - The Markdown Plugin I is no longer supported
  - The Kaizen Script functions are no longer supported

- **Version 2.2.8** (2023-05-08)
  - Installer updated for Flare 2023

- **Version 2.2.7** (2023-02-15)
  - The Quick Word feature now uses .docx instead of .doc

- **Version 2.2.6** (2022-11-11)
  - If the tag replacer comes across a topic without a body tag, it will now provide a better error message
  - Correction related to spaces in the accept/reject all changes

- **Version 2.2.5** (2022-10-19)
  - Leading and trailing spaces are now properly handled when accepting/rejecting all changes in a project

- **Version 2.2.4** (2022-08-18)
  - The "bookmark topic and create TOC" functions no longer ignore sup/sub tags

- **Version 2.2.3** (2022-05-31)
  - The QuickWord/PDF/HTML doesn't support non-default output files or folders: added error message

- **Version 2.2.2** (2022-02-26)
  - Fix to the problem that caused the Quick PDF/Word to sometimes fail in Flare 2021r3
  - Fix to the problem where condition export would not work in Flare 2021r3
  - Build a "Quick HTML" target for a CleanXHTML version of the topic you have open

- **Version 2.2.1** (2021-12-13)
  - Updated the Kaizenscript functionality so that you can re-install a script without deleting the existing DLL file first

- **Version 2.2.0** (2021-11-02)
  - Redesigned KaizenScript functionality for faster and easier deployment of custom add-ons
  - Bug fix related to the MadCap prefix in the tag replacer destination field

- **Version 2.1.4** (2021-10-20)
  - Fixed a bug in the TO DO notes function affecting the Link Viewer
  - Removed the old Kaizen Script functionality
  - PDFs created by the Quick PDF feature now get a unique name
  - The condition tag export now supports condition tags with special characters

- **Version 2.1.3** (2021-08-03)
  - The fast file search normal search is now case insensitive

- **Version 2.1.2** (2021-07-23)
  - Bug fixes

- **Version 2.1.1** (2021-07-09)
  - Fixed bugs related to replacing empty tags and target condition use export

- **Version 2.1.0** (2021-05-11)
  - Optimized the release flow

- **Version 2.0.7800.28098** (2021-05-11)
  - The installer now has silent mode enabled

- **Version 2.0.7786.20438** (2021-04-26)
  - Corrected bug related to creating a TOC and bookmarking the topic
  - Bug that would sometimes remove text when all changes were accepted

- **Version 2.0** (2021-04-09)
  - Added button to open a random topic or snippet

- **Version 2.0.7746.14208** (2021-03-17)
  - Clarified MD1 vs MD2 icons

- **Version 2.0.7745.39186** (2021-03-16)
  - Updated help call URL

- **Version 2.0.7738.17309** (2021-03-09)
  - Fixed a bug that causes the topic creator functionality to crash in some cases
  - Added small icons to buttons

- **Version 2.0.7735.36061** (2021-03-06)
  - New color icons that work better for dark mode

- **Version 2.0.7713.20478** (2021-02-12)
  - Various changes for the release of the separate docs for Markdown II

- **Version 2.0.7657.23742** (2020-12-18)
  - Corrected a bug when accepting all tracked changes in a project

- **Version 2.0.7653.21440** (2020-12-14)
  - Various bug fixes for the Markdown plugin
  - Fixes for the Sort TOC function and the Fast File Search function
  - The Validate XML function now supports all types of Flare files

- **Version 2.0.7592.23195** (2020-10-14)
  - Bug fixes and added config file to support differences in table import settings

- **Version 2.0.7577.23994** (2020-09-29)
  - Bug fixes related to the Markdown plugin license key

- **Version 2.0.7565.33411** (2020-09-17)
  - Bug fixes related to Markdown table import and the **Apply Links to TOC** function

- **Version 1.0.7433.19185** (2020-05-18)
  - Bug fixes related to To Do notes form buttons and Markdown table import

- **Version 1.0.7433.18756** (2020-05-08)
  - Bug fixes for Advanced Tag Replacer, Markdown export, and Tag replacer

- **Version 1.0** (2020-05-06)
  - Advanced Tag Replacer
  - Installation helper for KaizenScripts
  - Feature to convert Excel sheets to HTML tables
  - Google Calendar or Outlook reminders for topic review
  - Updated installer for Flare 2020
  - Bug fixes

- **Version 1.0** (2020-03-07)
  - Micro content import from Excel
  - Bug fixes

- **Version 1.0.7202.23531** (2019-09-20)
  - Bug fixes in relation to the updated Markdown plugin

- **Version 1.0** (2019-09-06)
  - Faster Tag Replacer
  - GUI changes
  - Batch setting for alt image texts
  - Statistics feature

- **Version 1.0** (2019-07-31)
  - Updates to the Markdown plugin
  - Bug fixes

- **Version 1.0** (2019-05-31)
  - Updated link to online help
  - Internal improvements to the Quick PDF functionality

- **Version 1.0** (2019-04-18)
  - Updated Accept/Reject all changes-functionality
