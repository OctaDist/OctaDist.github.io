---
layout: default
---
[back to homepage](./) | [manual](./manual.md)

## Error and Fixing

1. OctaDist Startup Slow? Windows Defender slow down OctaDist by scanning its file.
   You can fix this annoying issue by excluding OctaDist out of process scan list.
   
   Here are the steps for adding OctaDist to exclusion list:

   1. Go to Start > Settings -> Update & Security -> Virus & threat protection -> Virus & threat protection
   2. Under Virus & threat protection settings select Manage settings
   3. Under Exclusions, select Add or remove exclusions
   4. Select Add exclusion and specify the name of OctaDist executable, for example, 
      **"OctaDist-2.5.3-Win-x86-64.exe"** process for OctaDist. 
   5. Close OctaDist and run it again.

2. If program crashes with confusing errors messages, you may need to set `MPLBACKEND` environment variable 
   before running the program, like this:
   ```
   export MPLBACKEND=TkAgg
   ```

3. If error message says `ImportError:` or `ModuleNotFoundError:`, some important packages have not been installed. 
   To install all required packages, stay at top directory of OctaDist and type this command:
   ```
   pip install -r requirements.txt
   ```

[back to homepage](./) | [manual](./manual.md)
