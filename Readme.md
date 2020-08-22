ExtractInternetExplorerCompatibilityLogEvents.ps1
Copyright 2020 Elizabeth Greene <Elizabeth.a.Greene@gmail.com>
V0.01

Internet Explorer has a feature where it can log application compatibility events
This feature is enabled with the following registry key
Path: HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\Internet Explorer\Main\FeatureControl\Feature_Enable_Compat_Logging
Name: iexplore.exe
Type: REG_DWORD
Value: 1

Once that registry key is set and IE is restarted then the compatibility events are recorded to the Applications and Services\Internet Explorer event log.
This script reads a saved copy of that event log from a file, extracts the events, and converts them to human readable text.

This code worked for my application, extracting the path to a blocked ActiveX control.  That said, it is hack code that should not be used in any production capacity without attention by a competent developer.
Feel free to use or modify the code as long as it retains the author credit.  If you really want to make my day drop me a note and let me know if it worked for you.
