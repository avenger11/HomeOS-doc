---
title: Scene Card
layout: home
nav_order: 2
parent: Configuration
---

# Scene Card

![image](https://github.com/avenger11/HomeOS-doc/assets/37946892/d331030e-0cb6-4003-9a53-76b3d940dc85)
![image](https://github.com/avenger11/HomeOS-doc/assets/37946892/3760a99e-22bd-48aa-b48d-d746108d2d75)

### Files

- /homeos_module/scene

### Dependencies

- themes/homeos

### Configuration

For now, this card only support 4 scenes buttons. The configuration for this card is in homeos.yaml file at the top.
There is 2 fields to setup per scene:
- [ ] scene: reference an input_boolean to start/stop the scene
- [ ] icon: reference a .svg icon


        # Scene Configuration
        # +---+---+
        # | 1 | 2 |
        # +---+---+
        # | 3 | 4 |
        # +---+---+
        #
        # +----------+--------------------+-------------------------------------------+
        # | Name     | Anchor Name        | Entity or icon svg to change              |
        # +----------+--------------------+-------------------------------------------+
          scene1:       &config_scene1       'input_boolean.homeos_scene_clara_aux_dodo'
          scene1_icon:  &config_scene1_icon  'icon_moon_stars_fill'
        
          scene2:       &config_scene2       'input_boolean.homeos_scene_invite'
          scene2_icon:  &config_scene2_icon  'icon_wineglass_fill'
        
          scene3:       &config_scene3        'input_boolean.homeos_scene_morning_coffee'
          scene3_icon:  &config_scene3_icon   'icon_cup_saucer_fill'
        
          scene4:       &config_scene4        'input_boolean.homeos_scene_morning_coffee'
          scene4_icon:  &config_scene4_icon   'icon_empty'
