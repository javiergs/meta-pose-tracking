# MQTT configuration

The ASU25-ROVER Meta Quest APK documentation specifies:

- Broker: `broker.hivemq.com`
- TCP port: `1883`
- Topic: `jgs/unity/test`

The Java source currently subscribes to `tcp://test.mosquitto.org:1883` with the **same topic**. These brokers are different, so the current source configuration does not match the documented APK.

The visualizer expects JSON coordinate objects for `head`, `torso`, `hips`, `leftHand`, `rightHand`, `leftFoot`, `rightFoot`, `leftArmUp`, `rightArmUp`, `leftArmLow`, `rightArmLow`, `leftEye`, `rightEye`, `leftEyeGaze`, `rightEyeGaze`, and `cube`. Coordinate objects contain numeric `x` and `y` values; some include `z`.

Before publishing a paired release, verify the actual APK output and align the subscriber's broker, topic, and payload schema. Public MQTT brokers are for experiments, not private or sensitive tracking data.
