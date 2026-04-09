---
layout: default
title: API & Integrations
parent: Software
nav_order: 2
---

# API & Integrations

## MQTT
Publishes all available information:
- Pressures  
- Flowrates  
- Salinity  
- Temperatures  
- Output Status  
- Volumes
- etc.

Under topic: `yarrboard/brineomatic/*`

### Home Assistant

To use Brineomatic with Home Assistant, follow these steps:

* Install the Mosquitto Broker (MQTT server) app in Home Assistant.
* Enable MQTT discovery in Home Assistant
* In Brineomatic, enable MQTT and the Home Assistant features
* In Home Assistant, it should show the discovered watermaker

**TODO: add link to dashboard YAML here**

## Raw API

The protocol for communicating with Yarrboard is entirely based on JSON messages. Each request to the server should be a single JSON object, and the server will respond with a JSON object.

The protocol works over the following transport layers:

* HTTP API
* Websockets
* USB Serial
* MQTT

Here are some example commands you could send:

```
{"cmd": "start_watermaker"}
{"cmd": "stop_watermaker"}
{"cmd": "flush_watermaker"}
```

For detailed information on the Brineomatic specific protocol, see ```src/controllers/BrineomaticController.cpp```

Visit the [YarrboardFramework documentation](https://github.com/hoeken/YarrboardFramework#protocol) page for more details on the underlying protocol.

## SignalK
All the same data as MQTT, but in SignalK delta format with the `watermaker/brineomatic/*` path.

## Node-RED

One way to get battery level, tank level, and water temperature information into your watermaker is to use SignalK + Node RED using the HTTP API.  You can also use MQTT and have Brineomatic subscribe to a topic with that data.

[Download the Node-RED flow here.](https://raw.githubusercontent.com/hoeken/brineomatic/main/brineomatic_node_red.json)

![Node RED Flow]({{ '/assets/Node-RED flow.png' | relative_url }})
