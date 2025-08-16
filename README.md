This project is a sophisticated, real-time Intrusion Detection System (IDS) designed to classify network traffic as either benign or malicious. The system is built on Python and Flask, providing a local server that serves as both the IDS and a victim server for safe, controlled testing.

Methodology & Key Technologies
Machine Learning Model: The core of this system is a Random Forest Classifier (ids_model.pkl). This ensemble learning model, composed of multiple decision trees, is highly effective at identifying complex patterns in network data. It has been trained to recognize and distinguish between normal traffic and various attack types.

Data Preprocessing: A StandardScaler (scaler.pkl) is used to preprocess all incoming network data. This crucial step standardizes the features (e.g., Flow Duration, Flow Packets/s) to a common scale, which is essential for the model to make accurate and consistent predictions.

Server Framework: The entire system is hosted on a Flask server (ids_server.py). The server loads the trained model and scaler, processes real-time traffic, and provides an API endpoint for making predictions.

Testing and Validation
The system is tested in a controlled environment using Kali Linux as the operating system.

Victim Server: The Flask application is run on the Kali Linux machine, establishing it as the target for the simulated attacks.

Attack Simulation: To comply with safety and privacy policies, actual attacks are not performed. Instead, three distinct scripts are used to simulate network threats: a port scan, a brute-force attack, and a DDoS attack.

Real-Time Detection: As the simulated traffic hits the Flask server, the IDS model analyzes the data. Upon detecting a malicious pattern, an alert is immediately printed to the command-line interface, confirming the model's capability to identify and respond to threats in real-time.
