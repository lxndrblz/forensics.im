---
title: "Extracting Communication Artefacts from Microsoft Teams 1.X and Teams 2.X"
date: 2021-08-07T21:04:43+06:00
draft: false

# post author
author : "Alexander Bilz"

# post thumb
image: "images/blog/blog-2.jpg"

# meta description
description: "This post explains how communication artefacts from the IndexedDB of the Microsoft Teams desktop client can be extracted and written into a structured format."

# taxonomies
categories: ["Application Usage"]
tags: ["CLI","Windows", "Microsoft", "Teams 1.0", "Teams 2.0", "Parser", "Data Ingest", "Forensics"]
# post type
type: "post"
---
This post explains how forensically valueable communication artefacts, such as messages, appointments, contacts and call logs can be extracted from the *Microsoft Teams* desktop client and be written into a structured format *JSON* file.

The messages, message reactions, contacts and appointments can be extracted using the `ms_teams_parser.exe` available on [GitHub](https://github.com/lxndrblz/forensicsim/). The standalone parser enumerates the *IndexedDB* database and extracts all relevant records into a structured JSON file, which can be imported into another application.

The `ms_teams_parser.exe` has the following options.
* -f File path to the IndexedDB of Teams
* -o Destination where the output file is written

The `-f` parameter defines the location of the *IndexedDB* on the file system. These vary depending on the Teams client, the plan and the underlaying operating system that was used. The following table summarises the locations, where the *IndexedDB* can be commonly located.

| Client Version       | OS      | Path                                                                                                                                   |
|:---------------------:|:---------:|----------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft Teams 1.X | Windows | C:\Users\<username>\AppData\Roaming\Microsoft\Teams\IndexedDB\<url>.indexeddb.leveldb                                                  |
| Microsoft Teams 2.X | Windows | C:\Users\<username>\AppData\Local\Packages\MicrosoftTeams_8wekyb3d8bbwe\LocalCache\Microsoft\MSTeams\EBWebView\Default\IndexedDB\<url> |
| Microsoft Teams 1.X | macOS   | ~/Library/Application\ Support/Microsoft/Teams/IndexedDB/<url>.indexeddb.leveldb                                                       |
| Microsoft Teams 1.X | Linux   | ~/.config/Microsoft/Microsoft Teams/IndexedDB/<url>.indexeddb.leveldb                                                              |

The second required parameter is the output path. This parameter defines the location, where the parser writes the output file. This can be any valid *Windows* file path.

In summary, a sample command looks as following:
```text
.\ms_teams_parser.exe -f "C:\Users\johndoe\AppData\Roaming\Microsoft\Teams\IndexedDB\https_teams.microsoft.com_0.indexeddb.leveldb" -o "C:\Temp\John Doe.json"
```
The processing times depend on the size of the database and the number of records that have to be parsed. However, usually it should not take more than a few minutes. Once the parser is finished, the the *JSON* file can be imported into another application for further processing. The following screenshot shows a series of extracted messages that have been imported into *Excel*.

{{< figure src="/images/blog/parsed_indexeddb_imported_to_excel.png" alt="Parsed messages imported into Excel" caption="Parsed messages imported into Excel" class="big" >}}



