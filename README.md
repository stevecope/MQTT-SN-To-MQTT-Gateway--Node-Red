Current Gateways implement the full MQTT-SN protocol and although they work, they introduce an extra layer of complexity and generally require an MQTT connection per MQTT-SN client.

For this reason I created a simple node-red flow that functions as an MQTT-SN Gateway for MQTT-SN QOS 3 messages only.

The flow leverage's the existing packet creation and decode library code mqttsn-packet which can be downloaded here


Using this type of gateway simple MQTT-SN sensors can publish messages to MQTT clients.

The MQTT-SN sensor would not need to implement the full MQTT-SN Protocol stack.

With a bit of extra coding topic and messages filtering, and message combining could also be added.

There is a video here - https://youtu.be/SAiOIOHXN0I?si=ekZkwDOV_MqDDNL7

Settings Required

You will need to configure the UDP listener port and the MQTT broker IP address and port.

Application Areas

Any areas where you only need to publish data and not receive data.

It is particularly suited for lots of sensors as the gateway doesn't use a single MQTT connection for all MQTT-SN clients.
