---
title: "Installing the Microsoft Teams Parser for Autopsy"
date: 2021-07-06T16:04:43+06:00
draft: false

# post author
author : "Alexander Bilz"

# post thumb
image: "images/blog/blog-1.jpg"

# meta description
description: "This post explains how the Microsoft Teams parser for Autopsy can be installed."

# taxonomies
categories: ["Installation"]
tags: ["Autopsy", "Microsoft", "Teams", "Parser", "Data Ingest", "Forensics"]
# post type
type: "post"
---

This module requires the installation of Autopsy v4.18 or above and a *Windows*-based system.

To install the *Microsoft Teams* parser for *Autopsy*, please follow these steps:
* Download the `.zip` folder and the `.exe` file of the latest available [release](https://github.com/lxndrblz/forensicsim/releases).
* Extract the `.zip` folder onto your computer.
* Open the Windows File Explorer and navigate to your *Autopsy* Python plugin directory. By default, it is located under `%AppData%\autopsy\python_modules`.
* Create a new `forensicsim` folder within the `python_modules` folder.
* Copy the `ms_teams_parser.exe` and the `Forensicsim_Parser.py` to the `forensicsim` directory.
* Restart *Autopsy* to activate the module.

You can test verify that the module has been installed successfully by performing the following steps:
* Start Autopsy.
* Open/Create a case and add a source.
* You will find the added modules under the menu Tools -> Run Ingest Modules -> Name of the Data Source.

                