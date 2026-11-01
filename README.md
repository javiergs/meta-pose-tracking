# Meta Pose Tracking

Meta Quest pose tracking and Java desktop visualization over MQTT, for XR research and experimentation.

## Applications

- **Meta Quest tracker (`.apk`)** — publishes spatial tracking data from the headset.
- **Java desktop visualizer (`.jar`)** — subscribes to MQTT messages and displays a 2D projection of tracked body pose.

## Downloads

Download versioned application binaries from [GitHub Releases](https://github.com/javiergs/meta-pose-tracking/releases). A validated release has **not yet been published**; do not treat source-tree binaries as verified interoperable builds.

## Setup

See [installation](docs/installation.md), [MQTT configuration](docs/mqtt.md), and [troubleshooting](docs/troubleshooting.md).

## Source code

The Java desktop visualizer source is maintained separately in [jgs-lab/src-meta-pose-tracking](https://github.com/jgs-lab/src-meta-pose-tracking) (access may be restricted). This repository is for distribution and documentation, not application source.

## Project background

Originally developed as part of [CALHCI ASU25-ROVER](https://github.com/calhci/ASU25-ROVER). The Meta Quest APK and legacy desktop JAR were previously distributed as project resources.

## Status

Experimental research software. Before releasing the two applications together, verify that both use the same MQTT broker, topic, and message schema.
