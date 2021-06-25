---
layout: blocks
title: Homepage
date: 2017-11-22T23:00:00.000+00:00
page_sections:
- template: navigation-header-w-button
  block: header-2
  logo: "/uploads/2021/06/25/logo-2.png"
  navigation:
  - link: "#functions"
    link_text: Functionality
  - link: "#digest"
    link_text: Digest Add-in
  - link: "#messages"
    link_text: Messages
  - link: "#calls"
    link_text: Calls
  - link: "#meetings"
    link_text: Meetings
  cta:
    url: https://github.com/lxndrblz/forensicsim
    button_text: Get the Plugin
- template: hero-banner-w-image
  block: hero-2
  slug: features
  headline: uBuild <br><strong>design blocks</strong>
  content: The tool that allows you to build beautiful sites<br>all inside Forestry's
    content manager.
  cta:
    enabled: true
    url: https://github.com/forestryio/ubuild-jekyll
    button_text: 'See on GitHub '
  image:
    image: "/uploads/2018/06/21/product-shot-1.png"
    alt_text: Product Shot
  background_image: "/uploads/2018/06/21/hero-2-bg.png"
- template: content-feature
  block: feature-1
  media_alignment: Left
  slug: swap
  headline: <strong>Swap &amp; Switch<span class="light">&nbsp;</span></strong><span
    class="light">the Blocks to create sites quickly</span>
  content: Quickly assemble and create custom sites with 16 design blocks for seven
    different sections.
  media:
    image: "/uploads/2018/06/21/blocks-split.png"
    alt_text: uBuild Blocks Mock-Up
- template: content-feature
  block: feature-1
  media_alignment: Right
  slug: customize
  headline: <strong>Customize Blocks</strong><span class="light">&nbsp;to make quick
    edits throughout your new site</span>
  content: Each block comes with custom Front Matter that can be edited in Forestry
    CMS.
  media:
    image: "/uploads/2018/06/21/edit.gif"
    alt_text: Customize Blocks
- template: 1-column-text
  block: one-column-1
  slug: functions
  headline: 'The first Microsoft Teams Parser for Autopsy '
  content: Forensics.im is an Autopsy Plugin, which allows parsing <em>levelDB</em>
    of modern Electron-based Instant Messenger Applications like Microsoft Teams.
    Unlike the existing <a href="https://github.com/markmckinnon/Autopsy-Plugins/tree/master/Leveldb">levelDB
    plugin</a>, Forensics.im also parses the binary <em>ldb</em> files, which contain
    the majority of the entries and allows identifies individual entities, such as
    messages and contacts, and presents these in Autopsy's blackboard view.
- template: simple-footer
  block: footer-1
  content: Made with ❤︎ in Scotland

---
