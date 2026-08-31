# Hydroficient-IoT-Cyber-Defense-Externship
IoT cybersecurity project with Extern and Hydroficient, focused on securing a simulated hotel water-monitoring system through threat modeling, security testing, monitoring, and AI-based anomaly detection.

Below are my project deliverables, including threat analysis, security testing, technical documentation, and the final presentation.

## 1. Understanding IoT Systems & Threat Modeling
I analyzed the hotel water-monitoring system and its assets, applying STRIDE and CIA analyses to identify and prioritize security risks. The resulting threat model identified three primary risks: loss of availability, dashboard tampering, and unauthorized remote-control access.
#### Threat Model: 
https://docs.google.com/document/d/1KG85toLlbVbOf7Zy8L0iz3rfaxJhnlfk2MSuN2mLBuQ/edit?tab=t.0#heading=h.3i3su6ndfzs1

## 2. Building an Insecure MQTT Pipeline
I built an MQTT-based IoT pipeline using a local Mosquitto broker, Python publisher, and live subscriber dashboard to establish the baseline system. Security testing demonstrated that unprotected MQTT traffic could be intercepted in plaintext, exposing device IDs, locations, timestamps, and sensor values.
#### Vulnerability Assessment
https://docs.google.com/document/d/1HqZPZvueVIKvWwxhwJhoiJsElH7-kx_Y3M7GRptXWVs/edit?tab=t.0

## 3. Securing the Pipeline & Measuring the Cost
I secured the MQTT pipeline with TLS by configuring certificates for the broker and clients, then tested eavesdropping, invalid certificates, performance, and system load. The experiments demonstrated that TLS blocked eavesdropping while introducing only approximately 0.02% latency.
#### Experiment Results
https://docs.google.com/document/d/1bZm8I0rlkwVSRvQsKXQqggm6ze7l3L0JJzVOtVEhCw8/edit?tab=t.0

## 4. Enforcing Device Identity & Provisioning
I evaluated the limitations of one-way TLS and demonstrated how mutual TLS could restrict MQTT connections to authorized devices. I then developed a device provisioning policy covering certificate issuance, installation, verification, rotation, and device lifecycle management.
#### Device Provisioning Policy
https://docs.google.com/document/d/1PJL2j8W_ap9RIMVc_RG1vgfdEhCpCB0EjZHiXDZghTU/edit?tab=t.0

## 5. Defeating Replay Attacks
I tested timestamp freshness, sequence counters, and HMAC signing against immediate, delayed, and tampered replay attacks. After 12 experiments comparing different defense configurations, the combined use of all three protections blocked 100% of the tested attacks.
#### Defense Comparison Report
https://docs.google.com/document/d/1M2ZATiFlF9DLEMLQ03g-v8qxF4aUn55yujgL6vJBloI/edit?tab=t.0

## 6. Building a Real-Time Security Dashboard
I developed a real-time Streamlit dashboard to bring together system health, security events, and sensor behavior in a single view. The final dashboard incorporated AI-based anomaly detection using machine learning to identify unusual sensor behavior alongside existing security events.
#### Final Presentation 
https://docs.google.com/presentation/d/1BVU8YiiyFc30UPtITnpinOUvgvngoCgdUmNSJk4ORq0/edit?slide=id.p9#slide=id.p9


