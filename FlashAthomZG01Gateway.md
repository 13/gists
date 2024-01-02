# How to flash Athom ZG01 Zigbee Gateway

Set switches to serial mode [^1]
Connect DIO15 of RF-BM-2652P2 CC2652P2 to GND [^2]
Flash with cc2538-bsl-utility the flashfile "CC1352P2_CC2652P_launchpad_coordinator_20230507.hex" [^3]

```
docker run --rm \
    --device /dev/ttyUSB0:/dev/ttyUSB0 \
    -e FIRMWARE_URL=https://github.com/Koenkk/Z-Stack-firmware/raw/Z-Stack_3.x.0_coordinator_20230507/coordinator/Z-Stack_3.x.0/bin/CC1352P2_CC2652P_launchpad_coordinator_20230507.zip \
    ckware/ti-cc-tool -ewv -p /dev/ttyUSB0 --bootloader-sonoff-usb
```

### Sources
[^1]: https://zigbee.blakadder.com/Athom_ZG01.html
[^2]: https://www.athom.tech/forum/tasmota-related-1/athom-zg01-zigbee-gateway-how-to-flash-z-stack-firmware
[^3]: https://www.zigbee2mqtt.io/guide/adapters/flashing/flashing_via_cc2538-bsl.html
