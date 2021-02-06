# RichTextUnicode
Convert ASCII to rich text Unicode.

Based on the JavaScript [YayText](https://yaytext.com/)

Useful for making text 𝗯𝗼𝗹𝗱, 𝘪𝘵𝘢𝘭𝘪𝘤, 𝙗𝙤𝙡𝙙-𝙞𝙩𝙖𝙡𝙞𝙘, 𝓼𝓬𝓻𝓲𝓹𝓽, 𝚏𝚒𝚡𝚎𝚍-𝚠𝚒𝚍𝚝𝚑, 𝖋𝖗𝖆𝖐𝖙𝖚𝖗, ｆｕｌｌ-ｗｉｄｔｈ, and 🄱🄻🄾🄲🄺 on messaging programs like [Signal](https://signal.org/).

## Plasma KDE clipboard (klipper) actions

Add these commands to `~/.config/plasmashellrc` to get clipboard action functionality.

Select text like this:

\_Text I want bold\_

and choose, e.g., "bold" from the pop-up menu, and hit ctrl-v to paste over and you'll get

𝗧𝗲𝘅𝘁 𝗜 𝘄𝗮𝗻𝘁 𝗯𝗼𝗹𝗱

```
[Action_0]
Automatic=true
Description=Unicode rich text
Number of commands=8
Regexp=^_[^_]+_$

[Action_0/Command_0]
Commandline[$e]=echo "%s" | sed -e 's/^_//' -e 's/_$$//' | ~/RichTextUnicode 1
Description=bold
Enabled=true
Icon=
Output=1

[Action_0/Command_1]
Commandline[$e]=echo "%s" | sed -e 's/^_//' -e 's/_$$//' | ~/RichTextUnicode 3
Description=italic
Enabled=true
Icon=
Output=1

[Action_0/Command_2]
Commandline[$e]=echo "%s" | sed -e 's/^_//' -e 's/_$$//' | ~/RichTextUnicode 5
Description=bold italic
Enabled=true
Icon=
Output=1

[Action_0/Command_3]
Commandline[$e]=echo "%s" | sed -e 's/^_//' -e 's/_$$//' | ~/RichTextUnicode 7
Description=bold script
Enabled=true
Icon=
Output=1

[Action_0/Command_4]
Commandline[$e]=echo "%s" | sed -e 's/^_//' -e 's/_$$//' | ~/RichTextUnicode 9
Description=fixed width
Enabled=true
Icon=
Output=1

[Action_0/Command_5]
Commandline[$e]=echo "%s" | sed -e 's/^_//' -e 's/_$$//' | ~/RichTextUnicode 11
Description=bold fraktur
Enabled=true
Icon=
Output=1

[Action_0/Command_6]
Commandline[$e]=echo "%s" | sed -e 's/^_//' -e 's/_$$//' | ~/RichTextUnicode 12
Description=full width
Enabled=true
Icon=
Output=1

[Action_0/Command_7]
Commandline[$e]=echo "%s" | sed -e 's/^_//' -e 's/_$$//' | ~/RichTextUnicode 15
Description=block
Enabled=true
Icon=
Output=1
```
