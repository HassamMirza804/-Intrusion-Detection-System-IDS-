🛡️ ML-Powered Intrusion Detection System
This project is a real-time Intrusion Detection System (IDS) built to classify network traffic as either benign or malicious. The system is hosted on a local Flask server, which serves as both the IDS and the victim server for safe, controlled testing.

Key Components & Techniques
Random Forest Classifier: This is the core machine learning model (ids_model.pkl) used for classification. Random Forest is an ensemble learning method that combines multiple decision trees, making it robust and highly accurate for identifying complex attack patterns in network data.

StandardScaler: This data preprocessing tool (scaler.pkl) is crucial for preparing the network traffic data before it is fed to the model. It standardizes features like Flow Duration, Flow Packets/s, and Destination Port to ensure the model can make accurate and consistent predictions.

Flask Server (ids_server.py): The Flask application acts as the a central hub. It loads the trained model and scaler, processes incoming network traffic in real time, and provides an API endpoint for predictions.

How the System Works & Testing
To test the system, I use Kali Linux as the primary environment.

Server Hosting: The Flask server is run on Kali Linux, establishing it as the victim server.

Attack Simulation: Instead of performing actual attacks, I use scripts to safely simulate common network threats like port scans, brute-force attacks, and DDoS attacks.

Real-Time Detection: As the simulated traffic hits the Flask server, the IDS model analyzes the data. If a malicious pattern is detected, an alert is printed directly to the command-line interface (CLI), confirming the model's ability to identify and respond to threats in real time.
