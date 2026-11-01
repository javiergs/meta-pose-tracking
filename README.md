# Meta Pose Tracking

Meta Quest pose tracking and real-time desktop visualization using MQTT.

The Meta Quest application streams spatial tracking data; the Java desktop application receives those messages and displays a 2D representation of the tracked body pose.

![Java desktop visualization of Meta Quest tracking data](https://github.com/user-attachments/assets/5f57724f-ab13-4e36-be80-22f52257a03f)

## Applications

- **TrackerAllDevices.apk** — Meta Quest passthrough application with hand outlines and an interactive white cube. Users can grab and move the cube while tracking data is streamed over MQTT.
- **vero-MetaQuest-10.jar** — Java desktop MQTT subscriber that visualizes the received body pose.

## Downloads

The original application files are available in the [legacy directory](legacy/): [Meta Quest APK](legacy/TrackerAllDevices.apk) and [Java JAR](legacy/vero-MetaQuest-10.jar).

See [GitHub Releases](https://github.com/javiergs/meta-pose-tracking/releases) for versioned distributions when available. The original binaries are experimental and have not yet been validated together as a release.

## Getting started

Follow the [installation guide](docs/installation.md), then consult [MQTT configuration](docs/mqtt.md) and [troubleshooting](docs/troubleshooting.md).

## Source code

Java desktop visualizer source: [jgs-lab/src-meta-pose-tracking](https://github.com/jgs-lab/src-meta-pose-tracking) (restricted access may apply). The Unity project used to build the APK has not yet been identified in the source repository.

## Background

Developed in the context of the [CALHCI ASU25-ROVER](https://github.com/calhci/ASU25-ROVER) research project and reused in [ASU26-ROVER](https://github.com/calhci/ASU26-ROVER).

This is experimental research software. The documented APK broker differs from the broker currently configured in the Java source; check the [MQTT guide](docs/mqtt.md) before using both applications together.
