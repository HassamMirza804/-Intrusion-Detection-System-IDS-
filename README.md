### Intrusion Detection System
An Intrusion Detection System (IDS) is a security tool that monitors a computer network for suspicious activity and identifies potential threats. It acts as a vigilant guardian, analyzing traffic patterns to detect and alert you to unauthorized access or malicious behavior.

### Demonstration & Capabilities
A video demonstration of this project is available below.




The demonstration showcases the system's ability to detect and respond to simulated threats in real time. Due to security and privacy policies, actual attacks are not performed. Instead, three distinct scripts are used to simulate network threats: a port scan, a brute-force attack, and a DDoS attack.
As the simulated traffic hits the Flask server, the IDS model analyzes the data. Upon detecting a malicious pattern, an alert is immediately printed to the command-line interface, confirming the model's capability to identify and respond to threats.
# 🛡️ Phishing Detector

A real-time web application to identify and mitigate phishing threats in URLs, text, and files.

---

### 🎥 Demo Video

Here is a quick demo of the application in action.

https://github.com/user-attachments/assets/99d68d77-4b67-447f-b84a-48df5ce53250


### ✨ Features

* **URL Scanning**: Analyzes public and private URLs for suspicious keywords and structures.
* **Text Analysis**: Scans text from emails or messages to identify embedded phishing links.
* **File Scanning**: Processes `.txt` and `.pdf` files, using OCR to extract and analyze URLs, including those in images.
* **Deployment**: Hosted on Render for continuous availability and easy access.

---

### ⚙️ Technologies Used

* **Backend**: Python, Flask
* **Models**: Heuristic analysis, predefined phishing database
* **File Processing**: PyPDF2, pytesseract (OCR)
* **Deployment**: Render
* **Frontend**: HTML, CSS, JavaScript

---

### 🚀 Getting Started

To run this application locally, follow these steps:

1.  **Clone the repository**:
    ```sh
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name
    ```

2.  **Install the dependencies**:
    ```sh
    pip install -r requirements.txt
    ```

3.  **Run the Flask application**:
    ```sh
    gunicorn app:app
    ```
    The application will be accessible at `http://localhost:5000`.
