# 📧 Internal Office Messaging App 

Welcome to the **Internal Office Messaging App**, a  solution for office communication. This application allows for messaging between employees, even across different networks by utilizing a client-server architecture.

---

## 🌟 Features

- **Real-Time Messaging**: Communication with colleagues in real time.
- **Network Flexibility**: Operates across different networks by hosting the server on a cloud platform.
- **User-Friendly Interface**: Simple design for ease of use.

## 🚀 Getting Started

Follow these steps to set up the **Internal Office Messaging App** on your local machine.

### Prerequisites

- **Python 3.x**: Ensure that Python is installed on your system.

### Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/ThereseTaylor/Messaging-App.git
   ```

2. **Navigate to the Project Directory**:

   ```bash
   cd Messaging-App
   ```

3. **Install Dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

   *Note: If `requirements.txt` is not provided, ensure that the `socket` and `threading` modules are available in your Python environment.*

### Running the Application

1. **Start the Server**:

   ```python
   python server.py
   ```

   *The server will start and listen for incoming connections on `PORT` (default: 3389).*

2. **Start the Client**:

   In a separate terminal or on a different machine, run:

   ```python
   python client.py
   ```

   *You can start multiple clients to simulate different users.*


