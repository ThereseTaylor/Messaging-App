Production

This is a very basic messaging app that aims to enable a business to have an internal office messaging app. It can function even if the users are on different networks, the server side off the code will just have to be hosted on some cloud computing platform for that.

Our problem solving approach included doing research about how socket objects and ports work and how to implement it and how to host a server and what the different cloud computing options are. With this research as background we then implemented our solution.


# 📧 Internal Office Messaging App

Welcome to the **Internal Office Messaging App**, a streamlined solution for office communication. This application facilitates seamless messaging between employees, even across different networks by utilizing a client-server architecture.

---

## 🌟 Features

- **Real-Time Messaging**: Instant communication with colleagues in real time.
- **Network Flexibility**: Operates across different networks by hosting the server on a cloud platform.
- **User-Friendly Interface**: Simple and intuitive design for ease of use.

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

---

## 📄 Code Overview

### Client Code Highlights

The client script connects to the server, sends and receives messages, and has a user-friendly GUI built using Tkinter.

```python
# Example code snippet from the client
client = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
client.connect(('SERVER_HOST', 3389))
# Starts a new thread to listen for incoming messages
threading.Thread(target=listen_for_messages_from_server, args=(client,)).start()
```

### Server Code Highlights

The server script is a multithreaded application that handles multiple clients simultaneously, broadcasting messages to all connected clients.

```python
# Example code snippet from the server
server = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
server.bind((HOST, PORT))
server.listen(LISTENER_LIMIT)
# Accepts and handles new clients in a separate thread
threading.Thread(target=client_handler, args=(client,)).start()
```

---

## 🛠 Project Structure

```plaintext
Messaging-App/
├── client.py       # Client-side application
├── server.py       # Server-side application
└── README.md       # Project documentation
```

## 🤝 Contributing

Contributions are welcome! If you’d like to improve **Internal Office Messaging App**, please follow these steps:

1. **Fork the repository** and clone it locally.
2. **Create a new branch** for your feature:

   ```bash
   git checkout -b feature/YourFeature
   ```

3. **Commit your changes**:

   ```bash
   git commit -m 'Add new feature'
   ```

4. **Push to the branch**:

   ```bash
   git push origin feature/YourFeature
   ```

5. **Create a Pull Request** explaining your changes.

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

---

*Enhance your organization's communication with the Internal Office Messaging App today!*


