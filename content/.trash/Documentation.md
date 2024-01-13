---
tags:
  - MOC
---
# Obsidian
| Markdown        | Link                                                             |
|:--------------- |:---------------------------------------------------------------- |
| Basic syntax    | [Markdown Guide](https://www.markdownguide.org/basic-syntax/)    |
| Extended syntax | [Markdown Guide](https://www.markdownguide.org/extended-syntax/) |
| Hacks           | [Markdown Guide](https://www.markdownguide.org/hacks/)           |
| Attributes      | [Javalent](https://plugins.javalent.com/attributes)              |

<br>

| Plugins            | Link                                                        |
| :------------------ | :----------------------------------------------------------- |
| Dataview           | [GitHub](https://blacksmithgu.github.io/obsidian-dataview/) |
| Dataloom           | [GitHub](https://github.com/trey-wallis/obsidian-dataloom)                                                            |
| DB Folder          | [GitHub](https://rafaelgb.github.io/obsidian-db-folder/)                                                             |
| Map View           | [Github](https://github.com/esm7/obsidian-map-view#tip-copying-from-google-maps)                                                            |
| Note Refactor      |  [Github](https://github.com/lynchjames/note-refactor-obsidian)                                                            |
| Properties         | [Help Obsidian](https://help.obsidian.md/Editing+and+formatting/Properties)                                                            |
| Spaced Repetitions | [Stephen Wangi](https://www.stephenmwangi.com/obsidian-spaced-repetition/)                                                            |
| Templater          | [GitHub](https://silentvoid13.github.io/Templater/introduction.html)                                                            |
| DB Plugins Comp                   | [Google Docs](https://docs.google.com/spreadsheets/d/1k12D0MqAnReb035ipebisp45uK92ZetXy20DiY9PNAE/edit#gid=0)                                                             |

<br>

| Snippets / Classes | Link                                                                                               |
| :------------------ | :-------------------------------------------------------------------------------------------------- |
| Modular CSS Layout | [GitHub](https://github.com/efemkay/obsidian-modular-css-layout#installation--download-and-enable) |
| HTML Color block   | [GitHub](https://github.com/deathau/obsidian-snippets/tree/main)                         |
<br>

| DataView                | Code |
| ----------------------- | ---- |
| Inline dataview with JS | ` ```$=dv.list(dv.pages('#favourite').sort(f=>f.file.name,"asc").limit(4).file.link)``` `|

# Alfred
| Alfred   | Link                                                                                              |
| -------- | ------------------------------------------------------------------------------------------------- |
| Timer RH | [Dev](https://red-hot-timer-for-mac-os-x.3bitlab.com/add_timer_from_AppleScript_on_mac.html) |

# PDF Expert
| PDF Expert        | Link / Code                                                                                     |
|:----------------- |:----------------------------------------------------------------------------------------------- |
| PDF Expert script | [Mac Serial Junkie](https://www.macserialjunkie.com/forum/viewtopic.php?f=9&p=1156202#p1156202) |
| Alias             | ```alias pdfexpert_setup='zsh $HOME/Documents/PDFExpert_setup'```                               |
| Update & Patch    | ```pdfexpert_setup -u -p```                                                                     |
| Update            | ```pdfexpert_setup -u```                                                                        |
| Patch             | ```pdfexpert_setup -p```                                                                        |
| Download          | ```pdfexpert_setup -d```                                                                        |
| Version           | ```pdfexpert_setup -v```                                                                         |
| Help              | ```pdfexpert_setup -h```                                                                         |

# Dropbox

| Dropbox                        | Code                                                                     | Link                                                        |
| :------------------------------ | :------------------------------------------------------------------------ | :------------------------------------------------------ |
| Ignore file/folder from sync   | ` ```xattr -w com.dropbox.ignored 1 'path_to_file/folder_to_ignore'``` ` | [Dropbox](https://help.dropbox.com/sync/ignored-files) |
| Unignore file/folder from sync | ` ```xattr -d com.dropbox.ignored 'path_to_file/folder_to_unignore'``` ` | [Dropbox](https://help.dropbox.com/sync/ignored-files)                                                       |

# Wi-Fi

| DNS Provider        | DNS Server             |
| :---------- | :------------ |
| Pi-hole    | 192.168.1.60 |
| Cloudflare | 1.1.1.1      |
| Cloudflare | 1.0.0.1      |

###### See also
[[Shortcuts]]