---
title: "Event 2"
date: "2026-07-31"
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Saturday Meetup

## Event Information

| **Information**       | **Details**                                                                              |
| --------------------- | ---------------------------------------------------------------------------------------- |
| **Event name**        | Saturday Meetup                                                                          |
| **Time**              | 09:00 - 12:00, June 6, 2026                                                              |
| **Location**          | 26th Floor, Bitexco Financial Tower, 02 Hai Trieu Street, Sai Gon Ward, Ho Chi Minh City |
| **Role at the event** | Attendee                                                                                 |

---

## Summary of Content and Lessons Learned

### 1. Docker – A Containerization Technology

#### Speaker Information

> The speaker was **Bảo Huỳnh**, a Junior Cloud Native Developer at Endava Vietnam, Founder and Head of Lab at ITea Lab, and former Cloud DevOps Engineer at NAB Innovation Centre Vietnam.

#### Main Content

The presentation introduced the differences between virtualization and containerization.

Virtual machines provide strong isolation but require separate operating systems, consuming a significant amount of CPU, RAM, and storage. In contrast, containers are lighter because they share the host operating system.

Docker packages an application together with its libraries, dependencies, and configurations, allowing it to operate consistently across different environments.

The main components of Docker include:

- **Container:** A running instance of an application.
- **Image:** A template containing everything required to run an application.
- **Dockerfile:** A file that describes the steps required to build an image.
- **Layers and cache:** Features that make the build process faster and more efficient.

Docker is commonly used in CI/CD pipelines, microservices, development, testing, and cloud-native applications.

#### Lessons Learned

I gained a clearer understanding of the differences between virtual machines and containers. Docker helps solve the problem of an application working on one computer but failing to run on another.

To use Docker effectively, it is necessary to understand fundamental concepts such as images, containers, Dockerfiles, layers, and cache.

---

### 2. Combining AWS WAF with Machine Learning for Cyber Attack Detection on AWS

#### Speaker Information

> The speaker was **Lê Hoàng Gia Đại**, a final-year student at HUTECH University who aims to become an AWS Cloud Engineer and Cybersecurity Engineer.

#### Main Content

The presentation introduced a solution that combines **AWS WAF** with a **Machine Learning-based NIDS** to detect cyberattacks.

AWS WAF protects websites, APIs, and applications from attacks such as:

- SQL Injection.
- Cross-site Scripting.
- Bot traffic.
- Brute-force attacks.
- Abnormal requests.

However, WAF mainly relies on predefined rules and signatures, which may be ineffective against zero-day attacks or behaviors that have not been previously identified.

A Machine Learning-based NIDS can analyze network traffic, detect abnormal behavior, and identify new attack patterns.

The model used the **CSE-CIC-IDS2018** dataset, which was processed through data cleaning, invalid value removal, class balancing, and train-test splitting.

The deployment architecture used several AWS services, including AWS WAF, Lambda, S3, CloudWatch, GuardDuty, Security Hub, and Kinesis Data Firehose.

#### Lessons Learned

AWS WAF is an important security layer, but it should not be used as the only protection mechanism. Combining WAF with Machine Learning allows the system to detect abnormal behavior more flexibly.

Data quality directly affects the performance of a Machine Learning model. Therefore, data preprocessing and class balancing are essential steps.

---

### 3. AWS Neptune for Building a Graph Knowledge Base for GraphRAG

#### Speaker Information

> The speaker was **Việt Phát**, an Artificial Intelligence student at Swinburne University of Technology.

#### Main Content

The presentation introduced **GraphRAG**, an approach that combines Retrieval-Augmented Generation with a knowledge graph.

Traditional RAG retrieves relevant text passages to provide additional context to a Large Language Model. However, it may struggle with questions that require reasoning across multiple entities and relationships.

GraphRAG represents:

- Entities as **nodes**.
- Relationships as **edges**.

This structure allows the system to perform multi-hop reasoning and answer questions involving complex relationships more effectively.

Two implementation approaches were introduced:

- **Fully Managed Route:** Uses Amazon Bedrock Knowledge Bases and Amazon Neptune Analytics.
- **Custom Route:** Uses LlamaIndex together with Amazon Neptune.

#### Lessons Learned

GraphRAG is suitable for systems containing data with many entities and relationships.

The fully managed route enables faster deployment and reduces operational work, while the custom route provides greater flexibility but requires more technical skills and resources.

---

### 4. Multiplayer in the Cloud – Connecting Godot Clients with AWS WebSockets

#### Speaker Information

> The speaker was **Nguyễn Quốc Bảo**.

#### Main Content

The presentation introduced how to connect Godot clients to AWS WebSockets to build a cloud-based multiplayer game.

Three multiplayer networking approaches were discussed:

- **UDP/ENet:** Suitable for FPS or racing games that require low latency.
- **HTTP Polling:** Simple to implement but has higher latency.
- **WebSocket:** Suitable for turn-based games, lobbies, chats, and matchmaking.

The system architecture included:

- Godot Client.
- API Gateway WebSocket.
- AWS Lambda.
- Amazon DynamoDB.
- Amazon CloudWatch.

Lambda handles player connections, disconnections, matchmaking, player choices, and sending results back to both clients.

DynamoDB stores information such as `connectionId`, `status`, `opponentId`, `choice`, and `createdAt`.

#### Lessons Learned

The choice of multiplayer architecture should depend on the type of game being developed.

WebSocket combined with API Gateway and Lambda is suitable for simple turn-based games or matchmaking systems. However, a serverless architecture may not be appropriate for games that require real-time physics, continuous state management, and extremely low latency.

As the system scales, DynamoDB queries and stale connections must be managed efficiently. AWS GameLift should also be considered for more complex multiplayer games.

---

## Photos from the Event

Use discount code: AWS_50_Standard on the Tu Vi Dai Viet website

![Event photo](/images/4-EventParticipated/4.2-Event2/Bill.png)

![Event photo](/images/4-EventParticipated/4.2-Event2/AWS_50_STANDARD.png)