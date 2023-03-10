# Rivian Card for use in Home Assistant

A custom `picture-elements` YAML configuration with custom image layers to match the build of the Rivian vehicles.


## Features
All features of this card are visual alerts in nature. The following list will go through what to expect from this HA card.

- Supported Rivian Build Year Models:
    - R1T 2022/2023
- Vehicle Status:
    - Locked | Unlocked
    - Odometer
    - Home | Away
    - State of Charge (SoC)
- Window Rolled Down
- Exterior Door Open
    - front left (US: driver's door; Intl: passenger's door)
    - front right (US: passenger's door; Intl: driver's door)
    - rear left
    - rear right
- Exterior Closure Open Visual
    - tailgate
    - toneau cover (powered only)
    - frunk
    - gear tunnel (right and left)



## Installation

1. Copy the contents of [rivian-state-card.yml](https://github.com/tmack8001/ha-rivian-card/blob/main/src/custom-elements/rivian-state-card.yml) into a `picture-elements` lovelace card.
2. Modify the base R1T model based on your Rivian color (replace [rt1-launch-green.img](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-launch-green.png) with [rt1-rivian-blue.img](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-rivian-blue.png)). 
    - For instance, if you want to have your Home Assistant Rivian model to match your a specific color of your choosing.
    - Base Model Colors Supported and have the following image file name schema `https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-<color-name>.png`
        - [rt1-launch-green.img](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-launch-green.png)
        - [rt1-rivian-blue.img](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-rivian-blue.png)
        - [rt1-el-cap-granite.img](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-el-cap-granite.png)
        - [rt1-la-silver.img](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-launch-green.png)
        - [rt1-midnight.img](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-midnight.png)
        - [rt1-forest-green.img](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-forest-green.png)
        - [rt1-compass-yellow.img](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-compass-yellow.png)
        - [rt1-canyon-red.img](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-canyon-red.png)
        - [rt1-limestone.img](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-limestone.png)
        - [rt1-glacier-white.img](https://github.com/tmack8001/ha-rivian-card/blob/main/images/r1t/r1t-glacier-white.png)

## Credits and Contributions

Credit to [genosonic](https://community.home-assistant.io/u/genosonic) for the initially provided Rivian [images](https://community.home-assistant.io/t/generic-vehicle-card/397844/28) and [card concept](https://community.home-assistant.io/t/generic-vehicle-card/397844/5).