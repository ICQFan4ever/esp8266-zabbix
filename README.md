# esp8266-zabbix
Simple examples for creating zabbix-agent on ESP-devices

These components were used for development:

NodeMCU v3
DHT11
DS18B20


# dht11.ino
Simple script, including:
1) Reading temperature & humidity from DHT11 sensor (should work for DHT22 too)
2) Providing simple web-server for displaying them (routes are: "/", "/temperature", "/humidity")
3) Zabbix-agent on port 10050 with this items:
    - agent.ping
    - agent.hostname
    - agent.uptime
    - agent.version
    - read.temperature
    - read.humidity

# ds18b20-discover.ino
Simple script for detecting 64-bit addresses of DS18B20 sensors. Flash it & view address in console

# ds18b20.ino
Simple script, including:
1) Reading temperature from DS18B20 sensor
2) Providing simple web-server for displaying it (routes are: "/", "/temperature")
3) Zabbix-agent on port 10050 with this items:
    - agent.ping
    - agent.hostname
    - agent.uptime
    - agent.version
    - read.temperature
