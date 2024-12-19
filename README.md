# Multicasting Multimedia Over IP - Internet Radio

This project implements an Internet Radio system that streams multimedia content over IP using multicast. It allows multiple clients to connect to various radio stations, each broadcasting different content, mimicking real-life radio broadcasting over the internet.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Repository Structure](#repository-structure)
- [Installation](#installation)
- [How to Run the Project](#how-to-run-the-project)
- [Important Implementations](#important-implementations)
- [License](#license)

## Project Overview

The Internet Radio system is designed to simulate real-life radio broadcasting over IP networks using multicast. The server hosts multiple stations, each streaming different multimedia content. Clients can join these stations to receive live streaming, with functionalities to pause, resume, change stations, or terminate the connection.

## Features

- **Multicast Streaming**: Multiple clients can receive the same stream without additional server load.
- **Multiple Stations**: Server hosts multiple stations, each broadcasting different content.
- **Client Controls**: Clients can pause, resume, change stations, or terminate the connection.
- **Real-time Streaming**: Clients receive live multimedia streams from the server.

## Prerequisites

- A C compiler (e.g., GCC) installed on your system.
- Knowledge of network programming concepts.
- Required libraries for socket programming and multicast support.

## Repository Structure

- `Client/`: Contains the client-side code to connect to the server and receive streams.
- `Server/`: Contains the server-side code to broadcast streams to clients.
- `Project Report.pdf`: Detailed report explaining the project's design, implementation, and testing.

## Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/klsavaj/CN-Multicasting-Multimedia-Over-IP-INTERNET-RADIO-.git
   cd CN-Multicasting-Multimedia-Over-IP-INTERNET-RADIO
   ```

2. **Set Up the Environment**:

   - Ensure you have GCC installed. To install GCC on Linux, use:

     ```bash
     sudo apt-get install gcc
     ```

   - Install required libraries for multicast and socket programming (if not already available).

## How to Run the Project

1. **Compile the Server and Client**:

   Navigate to the `Server` and `Client` directories and compile the code:

   ```bash
   gcc server.c -o server
   gcc client.c -o client
   ```

2. **Run the Server**:

   Start the server to begin broadcasting stations:

   ```bash
   ./server
   ```

3. **Run the Client**:

   Start the client to connect to the server and interact with the stations:

   ```bash
   ./client
   ```

   Follow the on-screen instructions to connect to a station and control the stream.

## Important Implementations

- **Multicast Group Management**: The server manages multiple multicast groups, each representing a station. Clients join these groups to receive the corresponding streams.

- **Threading**: Both server and client use threading to handle multiple stations and client controls simultaneously, ensuring smooth streaming and user experience.

- **Socket Programming**: Utilizes UDP sockets for multicast streaming and TCP sockets for control messages between clients and the server.


## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
