# Rivian Card for use in Home Assistant

A custom `picture-elements` YAML configuration with custom image layers to match the build of the Rivian vehicles.


## Features
All features of this card are visual alerts in nature. The following list will go through what to expect from this HA card.

- Card Styles
  - Vehicle Door/Window Overview
  - Charging Session and Overview
- Supported Rivian Build Year Models:
    - R1T 2022/2023
    - R1S 2022/2023
- Vehicle State (icon and description):
    - Locked | Unlocked
    - Odometer
    - Home | Away
    - State of Charge (SoC)
    - Plugged In | Unplugged | Charging
- Overlays
  - Window Rolled Down
  - Exterior Door Open
      - front left (US: driver's door; Intl: passenger's door)
      - front right (US: passenger's door; Intl: driver's door)
      - rear left
      - rear right
  - Exterior Closure Open Visual (non-occupancy doors)
      - front trunk (eg. frunk)
      - charger door (*only while plugged in*)
      - gear tunnel (right and left)
      - tailgate
      - liftgate (r1s only)
      - tonneau cover (r1t - powered only)

**Features which require additional Lovelace Frontend dependencies**
- Pulsating Charge Status
- State of Charge Progress Bar



## Installation

**required minimum dependency** on [home-assistant-rivian v0.7.1](https://github.com/bretterer/home-assistant-rivian/releases/tag/0.7.1) for global lock/unlock state sensor

1. Choose if you want to have additional dependencies on HMAC Frontend components [card_mod](https://github.com/thomasloven/lovelace-card-mod) and [Bar Card](https://github.com/custom-cards/bar-card) (install if desired).

    1a. [no dependencies] Copy the contents of [rivian-r1t-state-card.yml](https://github.com/tmack8001/ha-rivian-card/blob/main/src/custom-elements/rivian-r1t-state-card.yml) into a `picture-elements` lovelace card. 

    1b. [with additional dependencies] Copy the contents of [rivian-r1t-state-card-dependencies.yml](https://github.com/tmack8001/ha-rivian-card/blob/main/src/custom-elements/rivian-r1t-state-card-dependencies.yml) (R1T) or [rivian-r1s-state-card-dependencies.yml](https://github.com/tmack8001/ha-rivian-card/blob/main/src/custom-elements/rivian-r1s-state-card-dependencies.yml) (R1S) into a `picture-elements` lovelace card. Features included in this markup and not the other include: progress bar battery state of charge visual and a pulsating charging icon visual. All other features are same as the other markup

2. Modify the base R1T model based on your Rivian color (replace [rt1-launch-green.png](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-launch-green.png) with [rt1-rivian-blue.png](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-rivian-blue.png)). 
    - For instance, if you want to have your Home Assistant Rivian model to match your a specific color of your choosing.
    - Base Model Colors Supported and have the following image file name schema `https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-<color-name>.png`
        - [rt1-launch-green.png](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-launch-green.png)
        - [rt1-rivian-blue.png](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-rivian-blue.png)
        - [rt1-el-cap-granite.png](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-el-cap-granite.png)
        - [rt1-la-silver.png](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-launch-green.png)
        - [rt1-midnight.png](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-midnight.png)
        - [rt1-forest-green.png](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-forest-green.png)
        - [rt1-compass-yellow.png](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-compass-yellow.png)
        - [rt1-canyon-red.png](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-canyon-red.png)
        - [rt1-limestone.png](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-limestone.png)
        - [rt1-glacier-white.png](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-glacier-white.png)

3. If you have used the Rivian (Unofficial) addon prior to v0.90, you will have to edit the entity names in the `picture-element` yaml to match the old entity names.  See old and new entity names here: https://github.com/bretterer/home-assistant-rivian/releases/tag/0.9.0.

## Credits and Contributions

Credit to [genosonic](https://community.home-assistant.io/u/genosonic) for the initially provided Rivian [images](https://community.home-assistant.io/t/generic-vehicle-card/397844/28) and [card concept](https://community.home-assistant.io/t/generic-vehicle-card/397844/5).
