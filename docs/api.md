---
layout: default
title: API & Integrations
nav_order: 6
---

# API & Integrations

## HTTP API
- Uses same JSON protocol / command structure as websocket.

## MQTT
Publishes all available information:
- Pressures  
- Flowrates  
- Salinity  
- Temperatures  
- Output Status  
- Volumes  

Under topic:  
`yarrboard/watermaker/*`

## WebSocket
Realtime interactive control of the machine.

## SignalK
All the same data as MQTT, but in SignalK delta format with the `watermaker/brineomatic/*` path.

## Node-RED

The easiest way to get tank level and water temperature information into your watermaker is to use SignalK + Node RED using the HTTP API.  

[Download the Node-RED flow here.](https://raw.githubusercontent.com/hoeken/brineomatic/main/brineomatic_node_red.json)

![Node RED Flow](/assets/Node-RED%20flow.png)
