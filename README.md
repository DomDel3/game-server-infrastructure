🖥️ Dedicated Game Server Infrastructure & Resource Optimization
Objective: To assemble, deploy, and administer a dedicated local server environment capable of concurrently hosting four independent, heavily modded game servers.

⚙️ Architecture & Hardware Specifications
CPU: Intel Core i7

Memory (RAM): 16GB DDR4 - Critical for multi-server hosting

Storage: 500GB Storage

Operating System: Linux

🛠️ Implementation & Configuration
Hardware Assembly: Co-assembled the physical machine, ensuring optimal cooling and component seating for 24/7 operation.

Environment Setup: Configured the Linux operating system and installed the necessary runtime environments (Java) to support the server instances.

Resource Allocation: Deployed four distinct server directories. Manually configured startup scripts to dynamically allocate appropriate RAM to each specific server based on its load and modpack requirements, carefully balancing the 16GB total limit.

Network Configuration: Verified internal IP addresses and configured port forwarding rules on the local router to ensure external players could connect to the correct server instances without IP conflict.

⚠️ Quality Assurance & Troubleshooting Log
Incident 1: Resource Exhaustion (Out of Memory)

Symptom: One of the heavily modded servers experienced severe rubber-banding (lag) and eventually crashed during peak player activity.

Diagnosis: Reviewed the crash logs and identified a java.lang.OutOfMemoryError. The server was hitting its memory ceiling due to resource-heavy modifications.

Resolution: Modified the server's initialization script to increase the maximum allocated heap size (e.g., -Xmx4G), balancing it against the total system RAM to ensure the other three servers remained stable.

Incident 2: Mod Incompatibility

Symptom: A newly applied modpack caused the server to refuse connection on startup.

Diagnosis: Isolated the issue by disabling mods in batches to identify the conflicting files.

Resolution: Removed the incompatible mod and verified server stability through localized playtesting before opening the network back up to end-users.

📈 Outcomes & Skills Demonstrated
This project provided hands-on experience in System Administration (Linux), Resource Management, Network Routing (Ports/IPs), and Root Cause Analysis.
