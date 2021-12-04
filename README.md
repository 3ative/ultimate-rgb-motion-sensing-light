# Ultimate RGB Motion Sensing light


```yaml
type: vertical-stack
cards:
  - type: custom:button-card
    styles:
      icon:
        - color: var(--button-card-light-color)
      card:
        - background: |
            [[[
              var red = states["number.light_shelf_red"].state;
              var green = states["number.light_shelf_green"].state;
              var blue = states["number.light_shelf_blue"].state;
              return 'radial-gradient(rgb(0,0,0,0%), 80%, rgb('+(red)+','+(green)+','+(blue)+')';
            ]]]
    tap_action:
      action: toggle
    entity: light.shelf_lights
  - type: vertical-stack
    cards:
      - type: entities
        entities:
          - entity: switch.auto_shelf_light
          - entity: number.light_shelf_red
            type: custom:slider-entity-row
          - entity: number.light_shelf_green
            type: custom:slider-entity-row
          - entity: number.light_shelf_blue
            type: custom:slider-entity-row
          - entity: number.light_shelf_brightness
            type: custom:slider-entity-row
          - entity: number.light_shelf_off_time
            type: custom:slider-entity-row
        state_color: false
        show_header_toggle: false
```
