# Optimal Placement of VNFs in MECs and SFC in Multi-Access Edge Computing Environment
## 1. Introduction
Mobile edge computing (MEC) and Network Function Virtualization (NFV) are emerging as key technologies to meet the demands of an expanding number of users in 5G.​ In NFV, the placement of VNFs is a crucial decision as it affects the performance, reliability and cost of the network.​ VNF placement and optimization play a crucial role in ensuring the efficient and effective operation of NFV enabled MEC nodes. Service Function Chaining (SFC) is a network architecture that enables the sequential processing of network traffic by a set of service functions.​ SFC involves the forwarding of network traffic to a set of service functions, such as firewalls, load balancers, in a specific order identified by policy, to provide a specific set of services to the traffic.​ SFC routes packets through a chain of network functions before reaching the destination.​

## 2. Motivation
The primary motivation for NFV enabled MEC networks is to address the limitations of traditional hardware-based network appliances.​ It improves network agility and new network services can be introduced easily.​ Service function chains provide a flexible and efficient framework for deploying network functions in a 5G network.​ SFC enables network operators to deploy network functions in a modular manner, providing a flexible framework for deploying network functions in a dynamic and changing network environment.​ SFC provides way to automate the virtual network connections can be set up to handle different types of traffic flows.​

## 3. Problem Statement
To design and implement cost-effective chaining of Virtual Network Functions (VNFs) in Multi-access Edge Computing (MEC) environment to create a Service Function Chain (SFC) such that latency constraints of every SFC are met.

## 4. Objectives
- To place VNFs in MEC servers such that resource constraint of every VNF is met.
- To create Service Function Chains for the optimally placed VNFs in an edge computing environment as per the requirements of various applications.
- To create an optimal Service Function Chain and satisfy the latency constraints of every SFC.

## 5. Results
### 5.1 Given:
#### 5.1.1 MECs:
| MEC  | CPU | RAM |
|------|-----|-----|
| MEC1 | 48  | 88  |
| MEC2 | 32  | 86  |
| MEC3 | 30  | 80  |
| MEC4 | 50  | 72  |
| MEC5 | 36  | 84  |

#### 5.1.2 VNFs:
| VNF     | CPU | RAM |
|---------|-----|-----|
| VNF1    | 2   | 8   |
| VNF2    | 4   | 16  |
| VNF3    | 8   | 32  |
| VNF4    | 6   | 48  |
| VNF5    | 10  | 20  |
| VNF1_   | 5   | 25  |
| VNF2_   | 4   | 20  |
| VNF3_   | 8   | 50  |
| VNF4_   | 2   | 35  |
| VNF5_   | 8   | 36  |
| VNF1__  | 10  | 48  |
| VNF2__  | 6   | 20  |
| VNF3__  | 8   | 40  |
| VNF4__  | 6   | 40  |
| VNF5__  | 8   | 48  |

### 5.2 VNF Placement in MEC using Genetic Algorithm

|MEC|Allocations|
|---|-----------|
|MEC1|[VNF2, VNF4, VNF5]|
|MEC2|[VNF2, VNF3, VNF2]|
|MEC3|[VNF1, VNF5, VNF1]|
|MEC4|[VNF4, VNF5, VNF1]|
|MEC5|[VNF3, VNF4, VNF3]|

### 5.3 Service Function Chaining using Q-Learning and SARSA Algorithms
Query: [VNF2, VNF5, VNF4, VNF3, VNF1, VNF3]

|Algorithm|Reward Function Value|Time(in sec)|Service Function Chain|
|---------|---------------------|------------|----------------------|
|Q-learning|34.56262|0.310210|[MEC2, MEC1, MEC4, MEC2, MEC4, MEC5]|
|SARSA|40.05592|0.289654|[MEC2, MEC1, MEC1, MEC2, MEC3, MEC2]|

## 6. Conclusion
VNF placement in MEC using Genetic algorithm improves the performance of edge computing networks by maximizing the deployment of virtual network functions near to end users. A low latency service function chaining leads to faster response time and reduced delay supporting many applications such as online gaming, video streaming, etc. We have implemented VNF placement using Genetic algorithm and Service Function Chaining using Q-learning and SARSA reinforcement algorithm. We have combined the results of VNF placement with the SARSA algorithm and obtained an optimal Service Function Chaining ensuring low latency. The proposed SARSA model is compared with the standard Q-Learning model. The comparison concludes that the proposed model outperforms the already existing Q-Leraning model for VNF placement and SFC chaining in Multi access Edge Computing environment.
