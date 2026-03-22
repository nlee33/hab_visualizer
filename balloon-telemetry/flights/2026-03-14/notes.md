# Flight Notes for 2026-03-14

Flight launched with following hardware:
  - Seeed Studio XIAO ESP32s3
  - WIO SX1262 LoRa Hat
  - BMP280 Environmental Sensor
  - ATGM336H GPS

Meshtastic with custom firmware, no change to device role (not set to Router mode)

--------------------------------------------------------------------------------------------

BMP280 either not reading, not sending or configured improperly
  - Did not receive any environmental readings at all, getting no humidity, pressure, tempearture data
  - Possible that the UART connections were reversed, ie TX -> TX , RX -> RX instead of TX -> RX , RX -> TX

--------------------------------------------------------------------------------------------

Possible next steps / goals:
  - Should remember to grab that dates wind graphs
  - Grab whatever data I can from the meshview page, and associated grafana charts
  - Consider adding an APRS node after getting HAM general license for payload recovery purposes
  - Two seperate boards, one to act as only a radio and another to act as a flight controller.
      - Flight controller should be able to grab all of the readings, which it will then tell the radio to send.
      - Ideally will have the readings for:
        - Temperature
        - Humidity
        - Pressure
        - Latitude
        - Longitude
        - Battery life
        - Consider adding an IMU for DoF readings to check if payload enclosure is properly doing the spiralling motion and creating drag, as well as providing acceleration/velocity readings.
  - Consider switching / adding a Meshcore node, as it is able to create rooms for nodes to live in as well as store   the last 30 messages sent, which will be helpful in logging the data from the ground station receiver.
  - 
