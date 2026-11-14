<div align="center">

# Shivam Singh

### Backend Engineer — Go · Real-Time Streaming · Kubernetes

**Systems that stay up under load.**
Dubai, UAE · UTC+4

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/shivam-singh-4946b2196/)
[![Email](https://img.shields.io/badge/Email-Get_in_touch-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:shivam2003sy@gmail.com)
[![LeetCode](https://img.shields.io/badge/LeetCode-Profile-FFA116?style=for-the-badge&logo=leetcode&logoColor=white)](https://leetcode.com/shivam2003sy)

</div>

---

## By the numbers

<div align="center">

| | | |
|:---:|:---:|:---:|
| **10,000+** | **15,000+** | **2 min → 2 sec** |
| concurrent streams in Go on Kubernetes | listings served under 3s, from timeouts | booking transaction latency |
| **10–20** | **~5 min** | **2×** |
| production servers on AWS EC2 | downtime per phase, Azure → AWS cutover | Smart India Hackathon wins |

</div>

---

## The system I'm known for

A real-time streaming pipeline in Go — many protocols in, one normalised model, many protocols out, holding 10,000+ concurrent streams on Kubernetes.

```mermaid
flowchart LR
    NTRIP[NTRIP] --> ING
    TCP[TCP client and server] --> ING
    UDP[UDP] --> ING
    FILE[File] --> ING

    ING[Ingest layer<br/>Go] --> NORM[Normalise<br/>one internal model]
    NORM --> PUB[Publish fan-out]

    PUB --> O1[MQTT]
    PUB --> O2[NTRIP]
    PUB --> O3[TCP and UDP]
    PUB --> O4[Socket and file]

    style ING fill:#00ADD8,stroke:#007d9c,color:#fff
    style NORM fill:#00ADD8,stroke:#007d9c,color:#fff
    style PUB fill:#326CE5,stroke:#1a4fb4,color:#fff
```

**The hard parts were not the happy path.** Malformed frames from one device cannot take down the listener, so bad events are isolated per event rather than per batch. Concurrent sessions stay thread-safe under sustained load. Every source identifier survives normalisation, so a problem traces back to the device that caused it.

---

## Tech

**Core**

![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)

**Streaming & messaging**

![MQTT](https://img.shields.io/badge/MQTT-660066?style=flat-square&logo=eclipsemosquitto&logoColor=white)
![Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![NTRIP](https://img.shields.io/badge/NTRIP-5C5C5C?style=flat-square)
![TCP/UDP](https://img.shields.io/badge/TCP%2FUDP-5C5C5C?style=flat-square)
![Spark](https://img.shields.io/badge/Apache_Spark-E25A1C?style=flat-square&logo=apachespark&logoColor=white)

**Infrastructure**

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)

**Data**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)

**Product**

![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=black)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white)

---

## Experience

<details>
<summary><b>Full-Stack Engineer</b> · Livjaza Vacation Homes Rental, Dubai · <i>May 2025 – present</i></summary>

<br/>

- Rebuilt search and listing infrastructure for **15,000+ listings**, from repeated timeouts to **sub-3-second** responses.
- Re-engineered booking logic to eliminate double-bookings under concurrent load — **2+ minutes → under 2 seconds**.
- Operate **10–20 production servers on AWS EC2**: self-hosted MongoDB replica sets with separated primary and secondary nodes, PostgreSQL, and tested backup and restore for both.
- Led a **phased Azure → AWS migration** — rebuilt on EC2, moved databases by full dump and restore, re-established replication, verified health before each cutover. Fully stable in three weeks, **~5 minutes downtime per phase**.
- Integrated three payment providers (Stripe, Tabby, Tamara) under PCI-compliant handling.

</details>

<details>
<summary><b>Full-Stack Engineer</b> · Lurra Systems, Australia (remote) · <i>Mar 2024 – Apr 2025</i></summary>

<br/>

- Designed and built the Go streaming pipeline diagrammed above — **10,000+ concurrent streams on Kubernetes**.
- Defensive network programming throughout: per-event isolation of malformed input, thread-safe concurrent sessions, configurable limits and timeouts.
- Built API-key IoT device management with live connection maps, coverage heatmaps and real-time metrics — device onboarding from days to minutes for non-technical staff.
- Authored the full Postman API documentation; measurably reduced inbound support requests.
- Reported directly to the CEO, turning business requirements into architecture.

</details>

<details>
<summary><b>Product Developer</b> · Central Ground Water Board, Govt. of India · <i>Aug 2023 – Feb 2024</i></summary>

<br/>

- Led a cross-functional team building an open-source hydro-chemical analysis platform in React and Electron — **[live on cgwb.gov.in](https://cgwb.gov.in/visualization-and-interpretation-of-hydro-chemical-data)**.
- Cut analysis time **30%** with interactive filtering, dynamic plotting and GIS-backed water-quality maps.
- Applied statistical methods and machine learning to predict contamination risk.

</details>

---

## Projects

<table>
<tr>
<td width="50%" valign="top">

### [InterviewBlitz](https://interview-blitz.vercel.app/)

Interview platform with scheduling, customised testing criteria, automated scoring and **real-time video over WebRTC**.

`React` · `Node.js` · `MongoDB` · `Express` · `WebRTC`

</td>
<td width="50%" valign="top">

### [Bloglite](https://vloglite.vercel.app/)

Social publishing platform with JWT auth, Redis caching, likes and comments.

`React` · `Node.js` · `MongoDB` · `Redis`

</td>
</tr>
</table>

<!-- PIN YOUR GO REPOS AND LIST THEM HERE, ABOVE THESE TWO.
     This section is the one recruiters judge you by. -->

---

## Recognition

🥇 **Winner — Smart India Hackathon 2023 (ISRO track)** · NTRIP caster, clients and servers for web and mobile
🥇 **Winner — Smart India Hackathon 2022 (Ministry of Jal Shakti)** · Team leader, hydro-chemical visualisation platform
🎓 **B.S. Data Science and Applications**, IIT Madras · **B.Tech Computer Science**, Bundelkhand University

---

<div align="center">

**Open to backend and infrastructure work.**

Happy to talk about anything involving Go, streaming, or systems that have to stay up.

</div>
