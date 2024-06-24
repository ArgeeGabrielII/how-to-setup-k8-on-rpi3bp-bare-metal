# Building a bare-metal Kubernetes Cluster on Raspberry PI 3B+

![RaspberryImage](/assets/img/rpi-image.jpeg)

## 2024-06-24 : Day 0

> [!NOTE]
> Please note that at the time of writing, the Raspberry Pi 5 has already been released. I am aware of this option, but I currently have three Raspberry Pi 3B+ units at my disposal. These should suffice for my purposes as I practice using Docker and Kubernetes.

### Goal

1. Install [K3s](https://k3s.io)

### Price Reference

For reference purposes, here's a list of parts and their price.

| Item                    | Unit Price (PHP) |
| ----------------------- | ----------------:|
| 3x Raspberry Pi 3b+     | Php 2,500.00     |
| 2x SanDisk 16GB MicroSD | Php 200.00       |
| 2x SanDisk 32GB MicroSD | Php 400.00       |
| 1x Power Cord           | Php 900.00       |
| 1x 3 Layer Cluster Case | Php 750.00       |
| **Total**               | Php 9,950.00     |

### Network Topology

![NetworkTopology](/assets/img/Network%20Topology.svg)

The nodes and router communicate through a network switch via wired connections, with the router providing Internet access via WiFi.

By keeping the cluster on a private network, I have full control over the IP addresses of each node, ensuring portability and ease of access across different networks without needing to reconfigure routers or my development environment.

Each node is assigned a static IP address, facilitating predictable and straightforward cluster node discovery. The router also acts as an Internet gateway, linking the local network to the Internet.

This setup simplifies management, as each node can be accessed easily and reliably through a consistent and organized network structure.

### Flashing OS Image

Will Flash the OS on each of the MicroSD Cards. I will use the [Raspberry Pi Imager v1.8.5](https://www.raspberrypi.com/software/).

I am going to use Ubuntu Server 24.04 LTS (64 BIT). I'm using ubuntu, because i'm some how familiar already with this.

