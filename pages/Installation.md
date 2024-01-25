---
title: Installation
layout: home
nav_order: 4
---

# Installation

I do recommend as a first step to install the following:
- All the required custom dependencies
- config.yaml
- homeos.yaml (simplify and remove all the cards, parameter and create some fake custom:button-card instead)
- theme folder

Once the 2 grids systems works it become easier to integrate card by card and configuring this to work with your installation.


### How to adapt to your wall tablet resolution

First get the height of the screen you will be using. This dashboard is not responsive.
Once you have this information add it to the general_theme.yaml

    # +----------------------------------------------------------------------------+
    # | Layout variable                                                            |
    # +----------------------------------------------------------------------------+
      homeos-screen-height: 800px #FireHD height

And you can play with the following values to adapt the result of the grid

      homeos-topbar-height: 3.5vw 
      homeos-appsbar-width: 6vw
      homeos-card-grid-gap: 0.6vw

The last theme variable is the formula to ensure you have square tile.

      homeos-card-grid-square: calc( (var(--homeos-screen-height) - var(--homeos-topbar-height) - (6 * (var(--homeos-card-grid-gap))))/5 )
