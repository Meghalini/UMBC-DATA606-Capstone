# Anomaly Detection using KDD99 Cup Dataset

## <i>Prepared for UMBC Data Science Master Degree Capstone by Dr Chaojie Wang.</i>

## Author
- Meghalini Gurram

### Github - https://github.com/Meghalini/UMBC-DATA606-Capstone.git

### LinkedIn - https://www.linkedin.com/in/meghalini-gurram-850b24240

### PPT Link - 

### Youtube Link - 


# About
Network anomaly/intrusion detection refers to the process of identifying and responding to suspicious or malicious activities on a computer network. It involves monitoring network traffic and analyzing it for signs of abnormal behavior or unauthorized access attempts.
There are various techniques and tools used in network anomaly/intrusion detection, including:

1. Signature-based detection: This approach involves comparing network traffic patterns and behaviors against a database of known attack signatures. If a match is found, it indicates a potential intrusion.
2. Anomaly-based detection: This technique focuses on identifying deviations from normal network behavior. It establishes a baseline of normal activity and raises an alert when there is a significant deviation from the established baseline.
3. Heuristic-based detection: Heuristic detection involves using predefined rules or algorithms to identify suspicious activities. It may not rely on specific attack signatures but rather on general indicators of malicious behavior.
4. Machine learning-based detection: Machine learning algorithms can be trained to analyze network traffic and identify patterns associated with different types of attacks. This approach can adapt to new and unknown threats by continuously learning from new data.
5. Intrusion Prevention Systems (IPS): IPS systems work in real-time to detect and prevent network intrusions. They can automatically block or alert administrators about potential threats.
6. Network behavior analysis: This technique involves monitoring the behavior of network hosts and users to identify abnormal activities. It may include monitoring traffic flows, login patterns, resource usage, and communication patterns.
7. Packet inspection: Packet inspection involves analyzing the content and headers of individual network packets to detect signs of malicious activity. Deep packet inspection (DPI) can provide more detailed information about network traffic.

Network anomaly/intrusion detection systems are typically implemented as part of a comprehensive network security strategy. They work alongside firewalls, antivirus software, and other security measures to protect networks from unauthorized access, data breaches, and other cyber threats.

# Why it matters:
- Network Security: Anomaly detection is vital for identifying unusual or malicious activities in network traffic. Cyber attackers often employ novel techniques to exploit vulnerabilities, making it essential to detect abnormal patterns that may indicate a security threat.

- Preventive Measures: Early detection of anomalies allows for proactive responses, preventing potential security breaches before they can cause significant damage. It helps in strengthening the overall security posture of a system or network.

- Data Breach Prevention: Anomaly detection plays a crucial role in preventing unauthorized access and protecting sensitive information. Timely identification of anomalous behavior can help in mitigating the risk of data breaches and safeguarding user privacy.

- Resource Optimization: Identifying and addressing anomalies can optimize resource utilization by focusing on genuine threats rather than false alarms. This ensures that security resources are efficiently utilized without unnecessary disruptions to normal operations.

- Adaptability to Evolving Threats: With the dynamic nature of cyber threats, an effective anomaly detection system is essential for adapting to new and emerging attack strategies. It provides a proactive defense mechanism that can evolve alongside evolving threat landscapes.

# Problem Statement: 
The KDD99 Cup Dataset is designed for the detection of intrusions in a network. The problem is to develop a robust anomaly detection system capable of distinguishing between normal network behavior and abnormal activities, which may indicate a potential intrusion. The dataset contains a mix of normal and malicious network traffic, presenting a challenging scenario for algorithmic detection.

## Challenges:

- Imbalanced Data: The dataset is imbalanced, with a small percentage of instances representing actual attacks. This imbalance poses challenges in training models that can effectively discern between normal and malicious activities.

- Diverse Attack Types: The dataset includes various types of attacks, ranging from denial-of-service to probing and unauthorized access. An effective anomaly detection system needs to be capable of detecting a broad spectrum of attack patterns.

- Real-time Detection: In practical scenarios, anomaly detection must operate in real-time to provide timely responses to potential security threats. This adds an additional layer of complexity to the problem, requiring efficient and fast algorithms.

- Adaptability: The system needs to be adaptable to new and evolving attack methodologies. As cyber threats continue to evolve, the anomaly detection system should be able to learn and adapt to new patterns of malicious behavior.


# Dataset
The KDD99 Cup dataset is a benchmark dataset for network intrusion detection. It consists of network traffic data collected from a simulated environment, containing both normal and various types of attack traffic. The dataset is divided into training and testing sets.

The dataset can be downloaded from the following link: KDD99 Cup Dataset

### Dataset Overview: 
The KDDcup99 dataset consists of network traffic data collected from a simulated environment, mimicking various types of attacks and normal network behavior. It comprises approximately five million connection records, with 41 features capturing different aspects of each connection, including source and destination IP addresses, port numbers, protocol types, and flags.

A benchmark dataset that is often utilized in the area of network anomaly/intrusion detection is the KDD Cup 99 dataset. It was developed as a component of the Knowledge Discovery and Data Mining (KDD) Cup competition, which was organized in 1999 with the goal of advancing study and advancement of intrusion detection systems.
The dataset includes network traffic data gathered from multiple sources and was created to replicate a computer network environment. It comprises both typical network connections and other harmful behaviors or assaults, including user-to-root (U2R), probe, and denial-of-service (DoS) attacks.

These are some of the main traits and qualities of the KDD Cup 99 dataset:

- Structure: The dataset consists of around 5 million distinct instances or records that reflect network connections. Each record is linked to a collection of characteristics or features that characterize network traffic. These characteristics or features include the protocol type, service, source and destination addresses, flags, and more.
- Attacking Types: DoS, probing, U2R, and regular connections are the four types of assaults that are included in the dataset. The normal category reflects appropriate network activity, whereas each assault category indicates destructive actions. Researchers may assess the effectiveness of intrusion detection systems in identifying and categorizing various sorts of assaults using these attack categories.
- Class imbalance is a well-known feature of the KDD Cup 99 dataset. Most occurrences fall within the typical group, although assaults are quite seldom. This class imbalance makes it difficult to create reliable intrusion detection models since the algorithms could be biased in favor of the dominant class.
- Preprocessing: To manage missing values, eliminate duplicates, correct inconsistencies, and turn the data into an appropriate format for analysis, the KDD Cup 99 dataset frequently needs preprocessing operations. Preprocessing methods are used to make sure the dataset is reliable and of high quality.


#### Data Dictionary:
Duration (continuous): The length of time for which a connection has been active.

Protocol Type (discrete): The type of network protocol used in the connection (e.g., TCP, UDP).

Service (discrete): The network service on the destination machine (e.g., http, ftp, telnet).

Flag (discrete): The status of the connection (e.g., normal, error, failed).

Src_bytes (continuous): The number of data bytes transferred from the source to the destination in the connection.

Dst_bytes (continuous): The number of data bytes transferred from the destination to the source in the connection.

Land (binary): Indicates whether the connection is from/to the same host/port; 1 if yes, 0 otherwise.

Wrong Fragment (continuous): The number of "wrong" fragments in the connection.

Urgent (continuous): The number of urgent packets in the connection.

Hot (continuous): The number of "hot" indicators in the connection.

Num Failed Logins (continuous): The number of failed login attempts.

Logged In (binary): Indicates whether the login was successful; 1 if yes, 0 otherwise.

Num Compromised (continuous): The number of compromised conditions in the connection.

Root Shell (binary): Indicates whether a root shell was obtained; 1 if yes, 0 otherwise.

Su Attempted (binary): Indicates whether the "su root" command was attempted; 1 if yes, 0 otherwise.

Num Root (continuous): The number of "root" accesses in the connection.

Num File Creations (continuous): The number of file creation operations in the connection.

Num Shells (continuous): The number of shell prompts in the connection.

Num Access Files (continuous): The number of operations on access control files.

Num Outbound Commands (continuous): The number of outbound commands in the connection.

Is Hot Login (binary): Indicates whether the login belongs to the "hot" list; 1 if yes, 0 otherwise.

Is Guest Login (binary): Indicates whether the login is a guest login; 1 if yes, 0 otherwise.

Count (continuous): The number of connections to the same host as the current connection in the past two seconds.

Srv Count (continuous): The number of connections to the same service as the current connection in the past two seconds.

Serror Rate (continuous): The percentage of connections that have "SYN" errors.

Srv Serror Rate (continuous): The percentage of connections to the same service that have "SYN" errors.

Rerror Rate (continuous): The percentage of connections that have "REJ" errors.

Srv Rerror Rate (continuous): The percentage of connections to the same service that have "REJ" errors.

Same Srv Rate (continuous): The percentage of connections to the same service.

Diff Srv Rate (continuous): The percentage of connections to different services.

Srv Diff Host Rate (continuous): The percentage of connections to different hosts among the connections to the same service.

Dst Host Count (continuous): The number of connections to the same host as the current connection.

Dst Host Srv Count (continuous): The number of connections to the same service as the current connection on the destination host.

Dst Host Same Srv Rate (continuous): The percentage of connections to the same service on the destination host.

Dst Host Diff Srv Rate (continuous): The percentage of connections to different services on the destination host.

Dst Host Same Srv Port Rate (continuous): The percentage of connections to the same service port on the destination host.

Dst Host Srv Diff Host Rate (continuous): The percentage of connections to different hosts among the connections to the same service on the destination host.

Dst Host Serror Rate (continuous): The percentage of connections to the destination host that have "SYN" errors.

Dst Host Srv Serror Rate (continuous): The percentage of connections to the destination service that have "SYN" errors.

Dst Host Rerror Rate (continuous): The percentage of connections to the destination host that have "REJ" errors.

Dst Host Srv Rerror Rate (continuous): The percentage of connections to the destination service that have "REJ" errors.

Target Variable (discrete): The class label indicating the type of connection, with categories such as normal, DoS (Denial of Service), Probe, R2L (Unauthorized access from a remote machine), and U2R (Unauthorized access to privileged user).

### Target Variable:
The target variable in the KDD99 Cup Dataset is the "Target Variable" or "Class," which represents the type of connection. This variable categorizes the network connections into different classes, including normal and various types of attacks such as DoS, Probe, R2L, and U2R. The goal of anomaly detection using this dataset is to accurately classify network connections into their respective classes, identifying any malicious activities.