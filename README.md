# Frient Keypad with Alarmo for Home Assistant with full key support

This project provides an automation to link a **Frient Keypad** to the **Alarmo** module in Home Assistant. It enables seamless communication between the keypad and Home Assistant's Alarm Control Panel, offering advanced functionality for home security management.

## Acknowledgements

Special thanks to:
- **Neliss** (https://community.home-assistant.io/t/zigbee2mqtt-control-alarmo-via-keypad/420016) for the original blueprint
- **Bygood91** (https://github.com/Bygood91/frient_keypad_alarmo) for adding additional functionality

I've combined their work to maintain Neliss's original logic while adding support for night mode and the SOS button functionality.

For French-speaking users, you can follow **Howmation**'s video tutorial (https://youtu.be/yFXBBJRfENc) which explains how to set up Neliss's blueprint, which served as the foundation for this enhanced version.

## Features

- **Arm All Zones**: Activate all zones with the **Lock** button.  
- **Arm Day Zones**: Activate day zones with the **Home** button.  
- **Arm Night Zone**: Activate night zones with the **Moon** button.  
- **Disarm**: Deactivate the alarm with the **Unlock** button.  
- **Emergency Mode**: Trigger an emergency by long-pressing the **SOS** button.  
- **Entry Delay**: The keypad emits beeps and flashes a green light during the entry delay.  
- **Exit Delay**: The keypad emits beeps and flashes a red light during the exit delay.  
- **Invalid Code**: Flashes an orange light when an incorrect PIN or RFID tag is used.  
- **Alarm in Progress**: Flashes a red light when the alarm is active.  
- **RFID**: Support for multiple PIN codes and RFID tags.

### RFID Tips:
- Use tools like [NFC Tools](https://play.google.com/store/apps/details?id=com.wakdev.wdnfc&hl=en&gl=US) (on Android) to read your RFID tags. Simply copy the tag ID (preceded by `+`) into the list of allowed PIN codes.  

## Setting up the SOS Button

The SOS button provides an emergency trigger option that can be configured to perform various actions when pressed. To set up this feature:

1. In the blueprint configuration, locate the "Emergency Action (SOS)" field under the actions section
2. Define the actions you want to trigger when the SOS button is pressed (examples: notify your phone, turn on all lights, trigger a siren, etc.)
3. The action will execute whenever the SOS button is long-pressed on your keypad

For all other configuration options and detailed setup instructions, please refer to Howmation's video tutorial linked above.

## Blueprint Preview

`![Blueprint Screenshot](images/blueprint.png)`

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.