---
title: "Week 1: Networking Challenge"
datePublished: Tue Feb 04 2025 14:58:54 GMT+0000 (Coordinated Universal Time)
cuid: cm6qlut8u000009l2fnk8frem
slug: week-1-networking-challenge
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1738680873724/6886d05c-5a23-47c8-9304-cbe008b5d039.png
tags: 90daysofdevops

---

## OSI and TCP/IP Models: 🌐📊

Networking is the backbone of our interconnected digital world. Whether you're browsing a website, streaming a movie, or sending an email, network models like the **OSI (Open Systems Interconnection)** model and the **TCP/IP (Transmission Control Protocol/Internet Protocol)** model are working behind the scenes to ensure seamless communication. In this blog, we’ll explore these **two models, Protocols, Ports and Essential networking commands for** **DevOps.**

---

### **What is the OSI Model?** 🌐✨

The **OSI model** is a conceptual framework that standardizes how data is transmitted across a network. It consists of **seven layers**, each with a specific function.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738680300629/966f560b-769a-470f-9e58-6164eb49a717.png align="center")

### **1\. Physical Layer**

* **Purpose**: Responsible for transmitting raw binary data (1s and 0s) over a physical medium such as cables or radio waves.
    
* **Example**: Ethernet cables transferring electrical signals or fiber optics transmitting light signals.
    

---

### **2\. Data Link Layer**

* **Purpose**: Ensures error-free data transfer between nodes within a local network by managing framing and physical addressing (MAC addresses).
    
* **Example**: A Wi-Fi router managing the transmission of data frames.
    

---

### **3\. Network Layer**

* **Purpose**: Manages the routing and forwarding of data packets between networks using logical addressing (IP addresses).
    
* **Example**: A router determining the best path for your data to travel to a web server.
    

---

### **4\. Transport Layer**

* **Purpose**: Provides reliable end-to-end communication, error checking, and flow control.
    
* **Example**: TCP ensures reliable file transfer, while UDP supports fast, live video streaming.
    

---

### **5\. Session Layer**

* **Purpose**: Establishes, maintains, and terminates communication sessions between applications.
    
* **Example**: Logging into a remote desktop or managing multiple browser tabs.
    

---

### **6\. Presentation Layer**

* **Purpose**: Converts data into a format readable by the application layer, handling encryption, compression, and translation.
    
* **Example**: SSL/TLS encrypting data for secure web browsing.
    

---

### **7\. Application Layer**

* **Purpose**: Interfaces with the user and provides network services like file transfer, email, and web browsing.
    
* **Example**: Using HTTP to load a webpage in a browser.
    

---

## **What is the TCP/IP Model?** 🌐📡

The **TCP/IP model** is a simplified framework compared to the OSI model, consisting of **four layers** that describe how data flows across the Internet.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1738680397122/0108ead9-ffb3-4874-8610-8736e4ca0d82.png align="center")

### **1\. Network Interface Layer**

* **Purpose**: Handles communication between the device and the physical network, combining functions of the Physical and Data Link layers from the OSI model.
    
* **Example**: Sending data through an Ethernet cable.
    

---

### **2\. Internet Layer**

* **Purpose**: Provides logical addressing and routes data packets across networks, similar to the OSI Network Layer.
    
* **Example**: IP assigns unique addresses to devices for communication.
    

---

### **3\. Transport Layer**

* **Purpose**: Manages data flow and ensures reliable communication, mirroring the OSI Transport Layer.
    
* **Example**: TCP guarantees error-free file downloads, while UDP supports live gaming.
    

---

### **4\. Application Layer**

* **Purpose**: Combines the Application, Presentation, and Session layers of the OSI model, delivering user-facing network services.
    
* **Example**: Using SMTP for email or HTTP for web browsing.
    

---

## **Comparison: OSI vs. TCP/IP**

| **OSI Layer** | **TCP/IP Layer** | **Real-World Example** |
| --- | --- | --- |
| Physical | Network Interface | Connecting a laptop to Wi-Fi or Ethernet. |
| Data Link | Network Interface | Ensuring error-free communication on a local network. |
| Network | Internet | Routing WhatsApp messages over the Internet. |
| Transport | Transport | Streaming Netflix without interruptions (TCP). |
| Session | Application | Secure login to a website (session management). |
| Presentation | Application | Decrypting data on an HTTPS-secured webpage. |
| Application | Application | Sending emails via Gmail using SMTP. |

---

## **Protocols and Ports for DevOps** 🚀🔧

### **1\. HTTP (Hypertext Transfer Protocol)**

* **Port Number**: 80
    
* **Purpose**: HTTP is the foundation of data communication on the World Wide Web. It is used to transfer web pages, images, and other resources between servers and clients.
    
* **Relevance in DevOps**:
    
    * Used in CI/CD pipelines for deploying web applications.
        
    * Monitoring web applications with tools like Prometheus and Grafana.
        
* **Example**: A DevOps engineer using an HTTP endpoint to fetch the status of a deployed service.
    

---

### **2\. HTTPS (Hypertext Transfer Protocol Secure)**

* **Port Number**: 443
    
* **Purpose**: HTTPS is the secure version of HTTP. It uses SSL/TLS to encrypt communication, ensuring data integrity and security.
    
* **Relevance in DevOps**:
    
    * Essential for deploying secure web applications.
        
    * Protecting APIs and sensitive data in automation scripts.
        
* **Example**: Configuring HTTPS for a Kubernetes Ingress Controller to ensure secure connections.
    

---

### **3\. FTP (File Transfer Protocol)**

* **Port Number**: 21
    
* **Purpose**: FTP is used to transfer files between a client and a server over a network.
    
* **Relevance in DevOps**:
    
    * Automating file uploads or downloads in pipelines.
        
    * Managing backups by transferring logs or artifacts to a remote server.
        
* **Example**: Using FTP to upload deployment packages to a legacy server.
    

---

### **4\. SSH (Secure Shell)**

* **Port Number**: 22
    
* **Purpose**: SSH provides secure remote login and command execution on servers.
    
* **Relevance in DevOps**:
    
    * Automating server management with Ansible or other configuration management tools.
        
    * Securely accessing cloud instances for troubleshooting.
        
* **Example**: A DevOps engineer using SSH to deploy an application on a remote server.
    

---

### **5\. DNS (Domain Name System)**

* **Port Number**: 53
    
* **Purpose**: DNS translates human-readable domain names into IP addresses, enabling communication over the Internet.
    
* **Relevance in DevOps**:
    
    * Managing DNS records for applications and services.
        
    * Troubleshooting connectivity issues in distributed systems.
        
* **Example**: Configuring DNS entries for a microservices architecture to enable service discovery.
    

---

## **Comparison of Commonly Used Protocols**

| **Protocol** | **Port Number** | **Primary Use Case** | **DevOps Relevance** |
| --- | --- | --- | --- |
| HTTP | 80 | Transferring web pages and resources | Monitoring and testing web applications |
| HTTPS | 443 | Secure communication over the web | Securing web and API communication |
| FTP | 21 | Transferring files between client and server | Automating file backups or transfers |
| SSH | 22 | Secure remote login and command execution | Server provisioning and automation |
| DNS | 53 | Resolving domain names to IP addresses | Service discovery and troubleshooting |

---

## Essential networking commands 🌐💻

### **1\. ping (Check Connectivity)**

### **Purpose**:

The `ping` command checks connectivity between your machine and another device on the network by sending ICMP echo request packets.

### **Usage**:

```bash
ping <hostname or IP address>
```

**Example**:

```bash
ping google.com
```

This command sends packets to Google’s server and checks if it's reachable, displaying response times and packet loss.

**Real-World Use**:

* Testing if a server or website is online.
    
* Diagnosing network issues by checking connectivity to a specific IP.
    

---

## **2\. traceroute / tracert (Trace Packet Routes)**

### **Purpose**:

`traceroute` (Linux/macOS) or `tracert` (Windows) traces the route packets take to reach a destination, showing each hop (router) along the way.

### **Usage**:

```bash
traceroute <hostname or IP address>  # Linux/macOS
tracert <hostname or IP address>    # Windows
```

**Example**:

```bash
traceroute google.com
```

This shows the path packets take to reach Google’s server, including response times for each hop.

**Real-World Use**:

* Identifying bottlenecks or slow points in a network.
    
* Diagnosing routing issues in multi-hop connections.
    

---

## **3\. netstat (Network Statistics)**

### **Purpose**:

The `netstat` command provides information about active network connections, routing tables, and network interfaces.

### **Usage**:

```bash
netstat -an
```

**Example**:

```bash
netstat -an | grep LISTEN
```

This shows all active listening ports on your machine.

**Real-World Use**:

* Checking which ports are in use and by which processes.
    
* Monitoring network activity to identify suspicious connections.
    

---

## **4\. curl (Make HTTP Requests)**

### **Purpose**:

`curl` is a command-line tool to transfer data using various protocols (HTTP, FTP, etc.). It’s commonly used to test APIs or download resources.

### **Usage**:

```bash
curl <URL>
```

**Example**:

```bash
curl https://api.github.com
```

This fetches the GitHub API’s response, which can be used to test connectivity and API configurations.

**Real-World Use**:

* Testing RESTful APIs.
    
* Downloading files or monitoring HTTP headers and responses.
    

---

## **5\. dig / nslookup (DNS Lookup)**

### **Purpose**:

These commands query DNS servers to resolve domain names into IP addresses and provide detailed DNS records.

### **Usage**:

#### `dig` (Linux/macOS):

```bash
dig <hostname>
```

**Example**:

```bash
dig google.com
```

#### `nslookup` (Windows):

```bash
nslookup <hostname>
```

**Example**:

```bash
nslookup google.com
```

These commands return the IP address of the specified domain and additional DNS information.

**Real-World Use**:

* Diagnosing DNS-related issues.
    
* Verifying DNS configurations for websites or services.
    

---

## **Summary of Commands**

| **Command** | **Purpose** | **Example Use Case** |
| --- | --- | --- |
| `ping` | Check connectivity | Test if a server is reachable. |
| `traceroute` / `tracert` | Trace packet routes | Identify network slowdowns or bottlenecks. |
| `netstat` | View network statistics | Monitor active connections and open ports. |
| `curl` | Make HTTP requests | Test APIs or download resources. |
| `dig` / `nslookup` | Perform DNS lookups | Resolve domain names and verify DNS configurations. |

---