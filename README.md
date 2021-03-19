# ha-ubee
[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg?style=for-the-badge)](https://github.com/custom-components/hacs)

This platform integrates [Ubee routers](https://www.ubeeinteractive.com/) into Home Assistant.

## Configuration
To use a Ubee router in your installation, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
device_tracker:
  - platform: ubee
    host: ROUTER_IP_ADDRESS
    username: YOUR_ADMIN_USERNAME
    password: YOUR_ADMIN_PASSWORD
```

### Configuration Variables
Variable | Required | Description
--- | :---: | ---
```model``` | ✗ | Ubee router model, e.g.,  `EVW32C-0N`. If omitted, model will be detected automatically. (Default: `detect`)
```host``` | ✓ | The IP address of your router, e.g., `192.168.1.1`.
```username``` | ✓ | The username of a user with administrative privileges, usually `admin`.
```password``` | ✓ | The password for your given admin account.

## Supported models:
- Ambit EVW320B
- Ambit EVW321B
- Ubee DDW36C
- Ubee DVW32CB
- Ubee EVW3200-Wifi
- Ubee EVW3226 (UPC)
- Ubee EVW32C-0N

## Note
By default, Home Assistant pulls information about connected devices from Ubee router every 5 seconds. See the [device tracker integration page](https://www.home-assistant.io/integrations/device_tracker/) for instructions on how to configure the devices to be tracked.

## Credits
Special thanks goes to [@mzdrale](https://github.com/mzdrale), the original author of the Home Assistant integration and current maintainer of the [pyUbee library](https://github.com/mzdrale/pyubee), on which this integration relies on.