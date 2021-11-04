# Ignition Edge at the I/O Level

## Inductive Automation Channel - [Video](https;//www.youtube.com/watch?v=OIS7nMBDnV0)

### 3 Goals for IIoT
1. Democratize Operational Data
2. Implement Cybersecurity Measures
3. Acheive desired business outcomes

### 3 Technologies for IIoT Success
1. Edge Computing
2. Networking (Zoning)
3. Data Communications

### groov RIO - I/O for the IIoT

- Remote Ethernet I/O for the IIoT
- 200,000+ I/O configurations from a single device
- Intelligent, remote Ethernet I/O
  - Multi-signal, multifunction I/O
  - 10-32 VDC power or PoE-powered
  - Web-based and cybersecure
  - Node-RED flow editor and runtime
  - Seamless integration with the Ignition
    - I/O data via MQTT w/ SpB or Modbus TCP
    - Ignition Edge v8
  - UL/ATEX, -20 to 70 degrees C operation, C1/D2
  - Terms
    - Sparkplug
    - MQTT
    - IngitionEDGE
    - groovMANAGE
- Ignition Edge v8 - Preinstalled
  - Edge IIoT Module - Preinstalled
    - MQTT Transmission
    - PLC device drivers (2 devices)
    - OPC-UA Server & Client
  - Additional module support
    - Edge Panel (1 remote client)
    - Edge Compute, Sync & EAM (Enterprise Asset Module)
    - Cirrus Link & Sepasoft Modules (GCP, AWS, Azure)
- Cybersecure, out of the box
  - User accounts
    - Local to device
    - LDAP managed
  - Network zoning
  - Configurable firewall for each network zone
  - Certificate management
- Software configurable I/O
  - 8 channels of mixed, multifunction I/O signals
    - Discrete ins and outs, self-wetting inputs
    - Current & voltage ins or outs
    - Resistance
    - Temperature
      - Thermocouples
      - Thermistors
      - ICTDs
    - 2 electromechanical relays - 5A/300V
      - Configurable as NO or NC

### Network Connections

- Eternet
- Wi-Fi
- OpenVPN Tunnel
- Network Options

### Firewall

- Each of the network interface can be designed to allow or disallow traffic
  - Can set the Protocol, Port, eth0, wlan0 and tun0 settings
- Different interfaces for the firewall
  - groov RIO
  - OptoMMP
  - ModbusTCP
  - Shell Access
  - Ignition Edge
  - Designer Access To Ignition Edge

### I/O Channels

- Form to set up the Channel that the I/O device is attached to
  - Name
  - Module Type
  - Channel Type
    - Shows you what channels are all supported when you click it!
  - Quality Indication
  - Feature
  - **Public Access**
    - State (Read)
    - On-Latch (Read)
    - Off-Latch (Read)
    - Counter (Read)
    - Writable (Read)
- When a public access attribute is set, the MQTT service will be advised of which channels and features are available to scan.
- 8 Channels of configurable I/O settings

### Ignition Edge

- Ignition and Ignition Edge platforms are both supported
- Authentication is built in
- Linux/arm device
- The Ignition Edge can see all of your networking resources, very thorough overview status page
- Gives you the option to connect to other systems
- Get data from one application to another
  - Gateway Network -> permit secure connections via the RIO controller
    - MQTT settings -> take all the tags in the RIO and publish them to a broker
    - 
