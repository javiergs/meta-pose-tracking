# Meta Pose Tracking

![Meta Quest](https://img.shields.io/badge/Meta-Quest-0467DF)
![Java 21+](https://img.shields.io/badge/Java-21%2B-blue)
![MQTT](https://img.shields.io/badge/MQTT-Streaming-660066)
[![Downloads](https://img.shields.io/badge/Download-Applications-green)](https://github.com/javiergs/meta-pose-tracking/tree/main/legacy)

Meta Quest pose tracking and real-time desktop visualization using MQTT.

The Meta Quest application streams spatial tracking data; the Java desktop application receives those messages and displays a 2D representation of the tracked body pose.

![Java desktop visualization of Meta Quest tracking data](https://github.com/user-attachments/assets/5f57724f-ab13-4e36-be80-22f52257a03f)

## Applications

- **TrackerAllDevices.apk** — Meta Quest passthrough application with hand outlines and an interactive white cube. Users can grab and move the cube while tracking data is streamed over MQTT.
- **vero-MetaQuest-10.jar** — Java desktop MQTT subscriber that visualizes the received body pose.

## Downloads

The original application files are available in the [legacy directory](legacy/): [Meta Quest APK](legacy/TrackerAllDevices.apk) and [Java JAR](legacy/vero-MetaQuest-10.jar).

See [GitHub Releases](https://github.com/javiergs/meta-pose-tracking/releases) for versioned distributions when available.

## Getting started

Follow the [installation guide](docs/installation.md), then consult [MQTT configuration](docs/mqtt.md) and [troubleshooting](docs/troubleshooting.md).
