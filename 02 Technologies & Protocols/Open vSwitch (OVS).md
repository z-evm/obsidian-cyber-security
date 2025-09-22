## 📜 Overview
**Open vSwitch (OVS)** is an open-source, multilayer virtual switch designed to enable network automation and support standard management interfaces and protocols (e.g., OpenFlow, OVSDB). It operates on various platforms, including **Linux, Hyper-V, and containers**, and is optimized for virtualized environments.

---

## ⚙️ Key Features

- **OpenFlow Support** – Enables SDN (Software-Defined Networking) control.
- **VLAN Tagging** – Supports 802.1Q VLANs and trunking.
- **Tunneling Protocols** – GRE, VXLAN, Geneve for overlay networks.
- **High Performance** – Kernel-based datapath acceleration.
- **Flow-based Forwarding** – Granular packet control via flows.
- **Port Mirroring** – For traffic monitoring and analysis.
- **Bonding & Load Balancing** – Aggregates multiple NICs.
- **QoS & Rate Limiting** – Traffic shaping and prioritization.

---

## 🏗 Architecture

| Component       | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| **ovs-vswitchd** | Main daemon implementing switch logic and handling datapath operations.   |
| **ovsdb-server** | Database server for configuration management.                             |
| **Datapath Module** | Kernel or userspace forwarding engine.                                 |
| **ovs-ofctl**   | CLI tool for managing OpenFlow rules.                                      |
| **ovs-vsctl**   | CLI tool for configuring OVS database and switch settings.                 |

---

## 🔌 Common Use Cases

- **Virtualized Data Centers** – Network virtualization for hypervisors.
- **Container Networking** – Kubernetes, Docker networking overlays.
- **SDN Deployments** – Integration with controllers (e.g., OpenDaylight, ONOS).
- **Traffic Monitoring** – Using SPAN/mirroring with IDS/IPS.
- **Multi-Tenant Isolation** – VLAN/VXLAN segmentation.

---

## 🛠 Basic Commands

```bash
# Show current OVS bridges
ovs-vsctl show

# Create a new bridge
ovs-vsctl add-br br0

# Add a port to a bridge
ovs-vsctl add-port br0 eth0

# Configure VLAN tag on a port
ovs-vsctl set port eth1 tag=10

# Add VXLAN tunnel
ovs-vsctl add-port br0 vxlan0 -- set interface vxlan0 type=vxlan options:remote_ip=10.0.0.2

# View flow entries
ovs-ofctl dump-flows br0
```

## 🔐 Security Considerations

- **Control Plane Protection** – Restrict access to OVS management interfaces.
- **Flow Rule Auditing** – Prevent unintended packet forwarding.
- **Tunneling Security** – Encrypt tunnels (e.g., IPsec) to prevent sniffing.
- **Segmentation** – Use VLAN/VXLAN to isolate tenant traffic.
- **Integration with Firewalls** – Combine with host- or network-based filtering.

---

## 📚 Related Topics

- [[Software Defined Networking (SDN)]]
- [[VLANs]]
- [[VXLAN]]
- [[Network Segmentation]]
- [[Hypervisors & Virtualization Networking]]

---

## 🏷 Tags

#ovs #networking #sdn #virtualization #ovsdb #openflow