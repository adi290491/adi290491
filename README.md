# Hi, I'm Aditya. 👋

### Senior Backend Engineer | Distributed Systems | Java & Go

I am a performance-obsessed software engineer with **9+ years of experience** building high-scale transactional systems. Currently architecting microservices at **Tata Consultancy Services** and diving deep into **Systems Programming** with Go.

I specialize in:
* **High-Throughput Systems:** Optimizing SQL and concurrency models to handle 1M+ daily events.
* **Distributed Architecture:** Designing fault-tolerant services using microservices, Kafka, and GCP.
* **Low-Level Engineering:** Building standard library-only tools to understand OS internals.

---

## 🛠️ Tech Stack

| **Core** | **Infrastructure** | **Data & Streaming** | **Observability** |
| :--- | :--- | :--- | :--- |
| ![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white) ![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white) | ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![K8s](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white) | ![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white) ![Kafka](https://img.shields.io/badge/Apache%20Kafka-000?style=for-the-badge&logo=apachekafka) | ![Dynatrace](https://img.shields.io/badge/Dynatrace-E6522C?style=for-the-badge&logo=Dynatrace&logoColor=white) ![Grafana](https://img.shields.io/badge/grafana-%23F46800.svg?style=for-the-badge&logo=grafana&logoColor=white) |

---

## 🚀 Featured Engineering Projects

### 1. [Systemic Productivity Planner](https://github.com/adi290491/productivity-planner)
> *Microservices, Event-Driven Architecture, & Performance Tuning*

A cloud-native ecosystem designed to decouple business logic into independent services (Session, Trend, Users). 
* **The Architecture:** Guarded by a custom **Reverse Proxy Gateway** built with Go's `net/http` and `httputil`.
* **The Challenge:** GORM reflection was causing high latency on write-heavy paths.
* **The Fix:** Migrated to **Raw SQL**, reducing P99 latency from ~100ms to 42ms.
* **Key Tech:** Go, Docker, PostgreSQL, Cloud Run, `sync.Mutex` Rate Limiter.

### 3. [Go Semantic Cache Gateway](https://github.com/adi290491/go-semantic-cache)
> *AI Infrastructure, Vector Search, & Latency Optimization

* **A cost-control firewall designed to intercept LLM traffic and serve responses from memory using vector similarity.
* **The Architecture: A "Dual-Path" retrieval engine that checks for Exact Matches (O(1)) and Semantic Matches (HNSW Index) before calling OpenAI.
* **The Challenge: Production LLM queries were averaging ~3,000ms latency and incurring high token costs for repetitive questions.
* **The Fix: Implemented Redis Vector Search with Cosine Similarity, reducing P99 latency to <50ms (~5,000x speedup) for cached hits.
* **Key Tech: Go (Goroutines), Redis Stack (RediSearch), OpenAI Embeddings, Docker.

### 2. [Go-Unix-Shell](https://github.com/adi290491/go-unix-shell)
> *Systems Programming, OS Internals, & Kernel Interfaces*

A POSIX-compliant shell built from scratch to master low-level system calls (`fork`, `exec`, `wait`).
* **Key Features:** Implements non-blocking pipelines (`|`) and I/O redirection (`>`, `>>`) by manually manipulating **File Descriptors**.
* **Why I built it:** To understand the abstraction layer between the Go runtime and the Linux Kernel.

---

## ⚡ Performance Benchmarks
*Results from `productivity-planner` load testing (via `hey`)*

| Metric | Result | Context |
| :--- | :--- | :--- |
| **Throughput** | **2,150 RPS** | Single Cloud Run instance (2 vCPU) |
| **P99 Latency** | **42 ms** | Optimized Raw SQL Write Path |
| **Error Rate** | **0.00%** | Sustained load over 5m duration |

---

## 📈 GitHub Stats

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=adi290491&show_icons=true&theme=radical&hide_border=true" height="150" alt="stats graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=adi290491&layout=compact&theme=radical&hide_border=true" height="150" alt="languages graph" />
</div>

---

<div align="center">
  <sub>Let's talk Systems Engineering. Connect with me on <a href="LINK_TO_YOUR_LINKEDIN">LinkedIn</a>.</sub>
</div>
