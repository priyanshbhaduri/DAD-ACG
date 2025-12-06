# DAD-ACG
The Adaptive Communication Glove (ACG) is a wearable, hand-based device designed to provide a highly intuitive and rapid communication method for individuals with speaking disorders.
# 1. Core Components
The device integrates several sensors and outputs, all managed by an Arduino Nano microcontroller:

MPU-6050 Gyroscope/Accelerometer: Measures the orientation and angle of the hand in 3D space, which corresponds to specific preset phrases.

Four Finger Flex Sensors: Used for digital triggering and mode selection.

LED Display Screen: Provides real-time visual feedback of the selected sentence and the device's current mode.

Speaker/Audio Module: Converts the text into audible speech using a Text-to-Speech (TTS) module.

# 2. Gesture-Activated Communication
The primary function relies on a two-factor activation system to ensure accurate, intentional communication:

Selection (Gesture): The user rotates or positions their hand into a specific angle (e.g., palm up, hand pointed forward). The gyroscope identifies this gesture pattern.

Confirmation (Trigger): The user must then bend the Index finger (Flex Sensor A0) to confirm the selection.

Output: Only when both the correct gesture and the trigger are active does the device instantly display the phrase on the screen and speak it aloud.

# 3. Advanced Communication Modes
The ACG utilizes the remaining flex sensors to implement mode switching, vastly increasing the number of available phrases without requiring complex new gestures.Finger/SensorFunctionDescriptionMiddle Finger (Flex Sensor A1)Mode A: NeedsActivates the sentence bank related to personal needs and requests (e.g., "I am hungry," "I need medication").Ring Finger (Flex Sensor A2)Mode B: SocialActivates the sentence bank for daily interactions and utilities (e.g., "Hello," "Thank you," "Yes," "No").Index Finger (Flex Sensor A0)Universal TriggerMust be bent to confirm the phrase selection in either Mode A or Mode B.

# 4. Emergency SOS Feature
A dedicated emergency feature is integrated into the Pinky finger to allow rapid, high-priority communication, bypassing the standard mode selection process.

Activation: The user bends the Pinky finger (Flex Sensor A3) five times within a 5-second window.

Action: This specific, repeated movement triggers an immediate override of all other functions, and the device broadcasts the high-priority message: "EMERGENCY: I need help immediately!" This design ensures the emergency message is only sent intentionally, not accidentally.
