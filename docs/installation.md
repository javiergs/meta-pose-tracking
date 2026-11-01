# Installation

## Meta Quest tracker

1. Enable Developer Mode on your Meta Quest headset.
2. Download the APK from the [releases page](https://github.com/javiergs/meta-pose-tracking/releases) once a validated release is available.
3. Install it using Meta Quest Developer Hub or `adb install <filename>.apk` with USB debugging enabled.
4. Launch the application. The original ROVER prototype displayed passthrough, a white cube, and hand outlines; users could manipulate the cube.
5. Connect the headset to a network that can reach the MQTT broker.

## Java desktop visualizer

1. Install Java (the legacy `vero-MetaQuest-10.jar` requires **Java 21 or newer**; the current source project targets Java 17).
2. Download a validated executable JAR from the [releases page](https://github.com/javiergs/meta-pose-tracking/releases).
3. Run `java -jar <filename>.jar` if the release is packaged as an executable JAR.
4. Confirm both applications use the same broker and topic before testing.

No verified binary pair has been published yet.
