# Troubleshooting

- **Headset not detected:** Enable Developer Mode and USB debugging; reconnect the USB cable and approve the debugging prompt. Try another computer or operating system if the prompt disappears.
- **No MQTT data:** Confirm headset network access, broker address, port `1883`, topic `jgs/unity/test`, and subscriber connection status.
- **Java compatibility error:** The original ROVER JAR requires Java 21 or newer; check `java -version`.
- **No visualization:** Verify that the MQTT message JSON matches the expected tracking schema and that publisher and subscriber connect to the **same** broker.

These notes are adapted from the ASU25-ROVER Meta Quest setup guide; behavior may differ for future releases.
