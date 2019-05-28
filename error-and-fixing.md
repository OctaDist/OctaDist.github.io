---
layout: default
---
[back to homepage](./) | [manual](./manual.md)

## Error and Fixing

1. If program crashes with confusing errors messages, you may need to set `MPLBACKEND` environment variable 
before running the program, like this:
   ```
   export MPLBACKEND=TkAgg
   ```

2. If error message says `ImportError:` or `ModuleNotFoundError:`, some important packages have not been installed. 
To install all required packages, stay at top directory of OctaDist and type this command:
   ```
   pip install -r requirements.txt
   ```

[back to homepage](./) | [manual](./manual.md)
