# Hydroficient-IoT-Cyber-Defense-Externship
IoT cybersecurity project with Extern and Hydroficient, focused on securing a simulated hotel water-monitoring system through threat modeling, attack testing, security monitoring, and AI anomaly detection. Below are my roject deliverables, including threat analysis, security testing, technical documentation, and the final presentation.

## 1. Understanding IoT Systems & Threat Modeling
The task presented a hotel water monitoring system and assets. I mapped system components, applied STRIDE and CIA analyses, and produced a threat model that prioritized three top risks: loss of availability, dashboard tampering, and unauthorized remote-control access.
#### Threat Model: 
https://docs.google.com/document/d/1KG85toLlbVbOf7Zy8L0iz3rfaxJhnlfk2MSuN2mLBuQ/edit?tab=t.0#heading=h.3i3su6ndfzs1

## 2. Building an Insecure MQTT Pipeline
I built an insecure MQTT pipeline, ran a local Mosquitto broker, published sensor messages from a Python publisher, and displayed them with a live subscriber dashboard. Traffic interception captured plaintext messages and revealed device ID, location, timestamps, and sensor values.
#### Vulnerability Assessment
https://docs.google.com/document/d/1HqZPZvueVIKvWwxhwJhoiJsElH7-kx_Y3M7GRptXWVs/edit?tab=t.0

## 3. Securing the Pipeline & Measuring the Cost
I added TLS to the MQTT pipeline, generated a CA and server certificates, reconfigured Mosquitto and updated clients. I ran four experiments (eavesdrop, bad certs, speed, stress) and produced measurements showing TLS blocked eavesdropping and added ~0.02% latency.
#### Experiment Results
https://docs.google.com/document/d/1bZm8I0rlkwVSRvQsKXQqggm6ze7l3L0JJzVOtVEhCw8/edit?tab=t.0

## 4. Enforcing Device Identity & Provisioning
I inspected the TLS config, identified that one-way TLS allowed any holder of the CA cert to connect, ran certificate-based attack scenarios, and produced a device provisioning policy and mTLS configuration to ensure only authorized devices could connect.
#### Device Provisioning Policy
https://docs.google.com/document/d/1PJL2j8W_ap9RIMVc_RG1vgfdEhCpCB0EjZHiXDZghTU/edit?tab=t.0

## 5. Defeating Replay Attacks
The work tested three replay defenses (timestamp freshness, sequence counters, HMAC signing) against immediate, delayed, and tampered replays. I ran 12 experiments, recorded block rates for each setup, and recommended deploying all three protections after the combined setup blocked 100% of tested attacks.
#### Defense Comparison Report
https://docs.google.com/document/d/1M2ZATiFlF9DLEMLQ03g-v8qxF4aUn55yujgL6vJBloI/edit?tab=t.0

## 6. Building a Real-Time Security Dashboard
I developed a real-time dashboard to monitor system health, security events, and anomalous sensor behavior using machine learning.
#### Final Presentation 
https://docs.google.com/presentation/d/1BVU8YiiyFc30UPtITnpinOUvgvngoCgdUmNSJk4ORq0/edit?slide=id.p9#slide=id.p9


