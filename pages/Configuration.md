---
title: Configuration
layout: home
nav_order: 5
---



# Change the position of a card within the grid area

This section is some information about how to move cards within the grid-template-area. The grid is a repetitive square of 8 by 5.
The size of a square is calculated within a formula in the general_theme.yaml file.

    # +----------------------------------------------------------------------------+
    # | Layout variable                                                            |
    # +----------------------------------------------------------------------------+
      homeos-screen-height: 800px #FireHD height
      homeos-topbar-height: 3.5vw
      homeos-appsbar-width: 6vw
      homeos-card-grid-gap: 0.6vw
      homeos-card-grid-square: calc( (var(--homeos-screen-height) - var(--homeos-topbar-height) - (6 * (var(--homeos-card-grid-gap))))/5 )



![image](https://github.com/avenger11/HomeOS-doc/assets/37946892/ea34fcb7-3abd-49b8-b99e-7bfc8f390352)



The position of a card within the grid is determinated by the name of the grid_area in homeos.yaml file.
If you want to modify the position of a cards, move the grid_area name.

            grid-template-areas: |
              "weather  weather  map map map map person_car person_bus"
              "weather  weather  map map map map garbage washer"
              "weather  weather  map map map map 3 ."
              "calendar calendar map map map map 4 ."
              "calendar calendar box box scene . 5 ."

By exemple, below is the code for including the Weather card within the grid. The grid_area is weather and you find the same reference within the grid-template-area. For now, ensure to keep the same card size, 2 square width by 3 square height for the weather card.

    # +----------------------------------------------------------------------------+
    # | Weather Area Definition                                                    |
    # +----------------------------------------------------------------------------+
                - type: custom:mod-card 
                  view_layout:
                    grid-area: weather
                  # the following style ensure the card resize to the grid
                  style: |
                    ha-card {
                      display: contents;   
                    }
                    :host {
                      margin: 0px !important;
                    }
                  card: !include homeos_module/weather/weather_card.yaml  
