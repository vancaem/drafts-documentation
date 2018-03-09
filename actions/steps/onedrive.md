---
title: Action Step – OneDrive
---

Create, append or prepend to files in [Microsoft's OneDrive service](http://onedrive.live.com). Note that more advanced OneDrive actions can also be scripted with the [OneDrive scripting support](https://github.com/agiletortoise/drafts-documentation/wiki/OneDrive).

## Examples

- [Save to OneDrive](http://drafts5-actions.agiletortoise.com/a/1D2)
- [Append to OneDrive Journal](http://drafts5-actions.agiletortoise.com/a/1D3)

## Options

- **Name**: Template for file name, including extension.
- **Path**: Path of folder, relative to OneDrive root, to place file. Default "/" is the root of your OneDrive folder. Should begin with "/"
- **Template**: Template for the content of the file.
- **Write Type**:
  - **create**: Create a new file. If an existing file already exists at the location, create as new file with a number suffix added.
  - **replace**: Create new file, overwriting an existing if it exists.
  - **prepend**: Prepend template content at the beginning of the file. Create the file if it does not already exist.
  - **append**: Append template content at the end of the file. Create the file if it does not already exist.
- **Identifier**: A string identifier for the OneDrive account to use. This value is only needed if you wish to use more than one OneDrive account with Drafts. If used, all actions with the same identifier will use the same alternate login for OneDrive.
