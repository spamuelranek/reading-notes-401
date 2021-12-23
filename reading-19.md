# AUTOMATION: WE ARE YOU'RE FRIENDS. PLEASE DO NOT RUN

## [Regex in Python](https://www.datacamp.com/community/tutorials/python-regular-expression-tutorial)
- in the library `re`

- Basic Patterns
- `re.match` returns a match object if there is a match or `None` if ther is not one

- `re.search` returns the first location where the regex hits
- `group` returns the the matched string

## [shutil - High-level File Operations](https://pymotw.com/3/shutil/)
- shutil
  - Purpose: High - level file operations

### Copying files
```python
import glob #?
import shutil

shutil.copyfile('taget_file.py','name_of_targets_copy_file.py)

```

- Copying files also takes in a third parameter
- Third_parameter = Defualt = 'Large blocks'
  - The defualt behavior is to read files in large blocks
- Third_parameter = -1
  - This is to read the block all at once
- Third_parameter = "some specified amount of block size"

- Powerful tool that will have to be referenced as needed

[Return Home](README.md)