# idumzaes/homebridge

Homebridge Docker image for aarch64 devices. Includes homebridge-config-ui-x plugin.

## Volume Persistance
Persistence is recommended to save data directory outside the container, as to not loose data.
Follow these steps to run this container.

`mkdir ~/homebridge_data` // Creates a directory on the host.

Run Container with the following command:

`docker run -dit --restart unless-stopped --network host --name homebridge -v ~/homebridge_data:/homebridge HOMEBRIDGE_CONFIG_UI=1 idumzaes/homebridge`
