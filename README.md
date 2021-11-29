# hass-blueprints

### presence-actions
Define a set of actions to run when a person leaves or arrives home. 

Requirements:
- `person.yourname` Entity with a state "home" for Home and "not_home" for Away. #Todo make this more flexible
[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fdbeltman%2Fhass-blueprints%2Fblob%2Fmaster%2Fpresence-actions.yaml)
##### 

### HVAC / CV Switcher
Switches between HVAC and CV installation depending on the outside temperature. 
Current threshold is at 8 degrees C as this seems to be the cutoff point for (my) HVAC's efficiency. Below that it has a chance to heat-cycle which is not optimal

Requirements:
- `input.boolean` Helper for Switching On and Off all functionality
- `input.number` Helper for setting the target temperature.
- `climate.yourCV` CV climate entity
- `climate.yourHVAC` HVAC climate entity
- `weather.yourlocation` Weather entity

