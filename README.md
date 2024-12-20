# Wireless Data Transmission Simulation
This project demonstrates how to wirelessly transmit real-time pipeline data to a remote dashboard.
## Approach
The approach for this project involves designing a system that efficiently collects, processes, and transmits real-time environmental data using a microcontroller and MQTT protocol. First, the microcontroller connects to a Wi-Fi network to enable wireless communication. A DHT22 sensor is interfaced with the microcontroller to measure temperature and humidity. 

The collected data is formatted into a JSON structure to ensure compatibility with MQTT messaging standards. To minimize unnecessary data transmission, the system compares the current sensor readings with the previous ones and only sends updates if a change is detected. 

The MQTT protocol is chosen for its low-latency communication, and the data is published to a specified topic on an MQTT broker. Remote monitoring is achieved by subscribing to the topic on an MQTT dashboard, allowing real-time visualization of the data. This modular and scalable approach ensures efficient and reliable wireless data transmission for IoT applications

## Features
- Collects real-time pipeline data such as pressure and temperature.
- Transmits data wirelessly using an MQTT protocol.
- Displays real-time data on a remote dashboard.
- Ensures efficient data transmission with low latency.
## Dashboard setup
The dashboard setup for this project involves using an MQTT client tool, such as the HiveMQ Websocket Client, to monitor the data being transmitted by the microcontroller. Here's how the setup is done:

- Access the Dashboard: Open the HiveMQ Websocket Client in a web browser or use any MQTT-compatible dashboard tool of your choice.

- Connect to the MQTT Broker: Enter the broker address (broker.mqttdashboard.com) and provide the credentials (username and password) defined in the code. In this case:
  - Username: myusername
  - Password: 8dKNFSGR4MWypNk
  - Subscribe to the Topic: Once connected, add a subscription to the topic used in the code (s). This allows the dashboard to receive and display the data being published by the microcontroller.
  > these credentials are Modifiable

- View Real-Time Data: As the microcontroller publishes temperature and humidity data to the topic, the dashboard will display the information in real-time.
  
By using the HiveMQ Websocket Client or similar tools, the setup allows users to visualize the transmitted data with minimal configuration, making it an ideal solution for prototyping and IoT development.
