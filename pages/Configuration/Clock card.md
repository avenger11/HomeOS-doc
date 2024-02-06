---
title: Clock Card
layout: home
nav_order: 3
parent: Configuration
---

# Scene Card

![image](https://github.com/avenger11/HomeOS-doc/assets/37946892/cf26347c-cd8e-4996-adc8-35a06dc57788)
![image](https://github.com/avenger11/HomeOS-doc/assets/37946892/2dc50480-5149-48b5-923d-be620c1cb3e6)

### Files

- /homeos_module/clock

### Dependencies

- themes/homeos

### Configuration

Add a time entity.

      - type: custom:button-card
        entity: sensor.time
        view_layout:
          grid-area: clock
        template:
          - template_clock
