# irremocon

ESPHome yaml file for IR remote control

Prototype 1st 

![103640](https://github.com/sevengivings/irremocon/assets/2328500/6b041d34-4c9b-482d-ab4d-394af27ba506)

Prototype 2nd 

Added light sensor to A0 pin for detection of operation of ourdoor unit. 
```
sensor:
  - platform: adc 
    pin: A0 
    name: "Outdoor Unit Operation"
    filters:
      - multiply: 3.3
    id: outdoor_operation

binary_sensor: 
  - platform: analog_threshold
    name: "On operation"
    sensor_id: outdoor_operation 
    threshold: 0.5
```

![082527](https://github.com/sevengivings/irremocon/assets/2328500/e5b55d88-bc67-4413-acda-001425ad428d)

Refer to https://imky.tistory.com/71 (in Korean) 
