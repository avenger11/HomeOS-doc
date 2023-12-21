---
title: Download
layout: home
parent: Setup
nav_order: 3
---

# Required Custom integration

This is the list of integration required for this dashboard.

* [Kiosk Mode](https://github.com/NemesisRE/kiosk-mode)
* [Button Card](https://github.com/custom-cards/button-card)
* [Layout Card](https://github.com/thomasloven/lovelace-layout-card)
* [Card Mod](https://github.com/thomasloven/lovelace-card-mod)
* [Atomic Calendar Revive](https://github.com/totaldebug/atomic-calendar-revive)
* [Swipe-Card](https://github.com/bramkragten/swipe-card)
* [Hui-Element](https://github.com/thomasloven/lovelace-hui-element)
* [custom-brand-icons](https://github.com/elax46/custom-brand-icons)


# Optional Custom integration 

I'm using alarmo as central alarm system but you can use your own.
* [Alarmo](https://github.com/nielsfaber/alarmo)

This is for the bus schedule on the person card.
* [GTFS-Realtime](https://github.com/zacs/ha-gtfs-rt)

# Apple Font Installation 

fonts.woff2 location: /www/fonts/
font.css location: /www/

Add in configuration.yaml

    lovelace:
      mode: yaml
      resources:
        [
           { url: '/local/fonts.css?v=2.1',type: css}
        ]

Add in general_theme.yaml

      # +----------------------------------------------------------------------------+
      # | Apple Fonts                                                                |
      # +----------------------------------------------------------------------------+
        primary-font-family: SF Pro Text, Roboto, system-ui
        paper-font-common-base_-_font-family: var(--primary-font-family)
        paper-font-common-code_-_font-family: var(--primary-font-family)
        paper-font-body1_-_font-family: var(--primary-font-family)
        paper-font-subhead_-_font-family: var(--primary-font-family)
        paper-font-headline_-_font-family: var(--primary-font-family)
        paper-font-caption_-_font-family: var(--primary-font-family)
        paper-font-title_-_font-family: var(--primary-font-family)
        ha-card-header-font-family: var(--primary-font-family)
        mdc-typography-body1-font-family: var(--primary-font-family)
        mdc-typography-font-family: var(--primary-font-family)  
