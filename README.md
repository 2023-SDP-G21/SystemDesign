# SystemDesign

## Design Ideas

1. The objective message from software to hardware should be in plain string or txt.
2. The warning message from hardware to software should be in json.
3. Embed LED to the hardware system, for battery level indication.

## API Design
### Data
Data will be transferred from the sensors to the software in a JSON string with 2 attributes: `type` and `payload`. The type will determine where the data is coming from.

Data that will be transferred from the sensors include
  - Battery Level
  - Speed
  - Acceleration

### Warnings / Messages
Messages and warnings will also be communicated to the software with this API. Example messages include
  - EMERGENCY_STOP
  - DISABLE_COMPONENT
  - COMPONENT_CONNECTION_LOST
