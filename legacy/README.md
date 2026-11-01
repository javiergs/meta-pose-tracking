# Meta Quest Setup Instructions

This guide explains how to install and run the **TrackerAllDevices** app on the Meta Quest headset, and how to verify that data is being streamed over MQTT.  
It also describes how to use the included **JAR application** to visualize the streamed data in real time.

## Files
- **TrackerAllDevices.apk** – This is the APK file you need to install on the Meta Quest headset.  
- **vero-MetaQuest-10.jar** – This is a Java desktop application that acts as an MQTT subscriber. It receives the data streamed from the headset and visualizes it by mimicking the user’s body posture. This allows you to see the data in real time on your computer, similar to the image below.

![meta-quest](https://github.com/user-attachments/assets/5f57724f-ab13-4e36-be80-22f52257a03f)


## Steps

### 1. Install Meta Quest Hub (MQH)
- Download and install **Meta Quest Hub** software from Meta:  
  [Meta Quest Hub Documentation](https://developers.meta.com/horizon/documentation/unity/ts-mqdh/)  
- MQH allows you to install APK apps onto your headset.

### 2. Install the APK
- Using MQH, install the APK file from our GitHub repository:  
  **TrackerAllDevices.apk**

### 3. Run the App
- Put on the headset and launch the installed app.
- You should see:
  - **Real-world objects** (e.g., your monitor, keyboard).
  - **Virtual overlays**:
    - A **white cube**.
    - **White contour outlines** of your hands.

- You can **manipulate the cube**:
  - Grab it with two fingers.
  - Move it around in space.

### 4. Data Streaming
- Once the app is running, it will stream data over MQTT.

  **MQTT Settings:**
  - **Topic:** `jgs/unity/test`
  - **Broker Address:** `broker.hivemq.com`
  - **Port:** `1883`

You can verify the stream using any MQTT client (e.g., [MQTT Explorer](https://mqtt-explorer.com/))  
or by running the provided **Java Desktop App (JAR file)** application to visualize the body posture.

> [!WARNING]
> The **`vero-MetaQuest-10.jar`** application requires **Java 21 or newer**.  
> Running it with an older Java version will cause a compatibility error, preventing the program from starting.

## Next Steps
- Complete the installation and confirm everything is working.
- Try running the JAR file to see the data stream in action.
- If you encounter issues, please reach out with questions.
- While following these steps, take notes on anything missing, unclear, or requiring additional setup. The goal is for others to be able to reproduce your installation smoothly.


## Troubleshooting & Tips
- **USB Link / Air Link:** Ensure your headset is connected to the computer either via USB cable (Link) or over Wi-Fi (Air Link).
- **Developer Mode:** Make sure Developer Mode is enabled in the Meta Quest mobile app.
- **APK Permissions:** The first time you launch the app, grant necessary permissions (camera, tracking, etc.).
- **MQTT Network Access:** Verify that your headset is connected to the internet so it can reach the MQTT broker.

> [!NOTE]
> If your Meta Quest 3 is not being recognized or the **"Allow USB Debugging" prompt briefly appears and then disappears**, the issue may be caused by a background process, driver, or system-level security application interfering with the ADB connection.  
> In my case, the prompt appeared once and then stopped showing up entirely when connecting to my Windows PC.  
> Fix: If you encounter a similar issue, try setting up on a **different operating system or computer** to isolate whether the problem is specific to your environment.
