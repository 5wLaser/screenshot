# screenshot
Minimal screenshot script for X

dependencies:
- `shotgun`
- `hacksaw`
- `basicrop` - optional, can be replaced

`shotgun` and `hacksaw` can be replaced with `maim` and `slop`. 
Replacing the editor is harder, but still straightforward. `basicrop` takes an input and output file, so if an editor can do something like that, then no real modding is needed.

## Usage
First, set `$fotoDir` to an appropriate default dir for your screenshots, and change `$foto` if you want a different default filename.
```
Usage: screenshot [options]

Options:
-o [OUTFILE]	specify an output file
crop		use crop/window select mode
temp		send file to /tmp for temporary storage and clipboarding
file		file-only, don't save image to clipboard
edit		edit the most recently-taken screenshot
```
## Examples
To crop a screenshot to out.png without copying to clipboard:

`screenshot crop -o out.png file`

To take a screenshot to out.png without the clipboard while cropping:

`screenshot -o out.png file crop`

To remove clipboard copying and take a cropped screenshot to out.png:

`screenshot file crop -o out.png`

To take a full screenshot to /tmp:

`screenshot temp`

To edit:

`screenshot edit` to save in `$fotoDir`, or `screenshot temp edit` to keep the result in /tmp
