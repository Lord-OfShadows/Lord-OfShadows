<h1 align="center">Hey, I'm Arjun 👋</h1>

<p align="center">
  <b>Final-year CS student · Open-source developer · Building systems that survive failure</b>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/arjunangirus"><img src="https://img.shields.io/badge/LinkedIn-arjunangirus-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="https://github.com/Lord-OfShadows"><img src="https://img.shields.io/badge/GitHub-Lord--OfShadows-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>
  <a href="https://codeforces.com/profile/EarnTHYPart"><img src="https://img.shields.io/badge/Codeforces-EarnTHYPart-1F8ACB?style=for-the-badge&logo=codeforces&logoColor=white" alt="Codeforces"></a>
</p>

---

## 🧑‍💻 About me

I'm a B.E. Computer Science and Engineering student at **Thapar Institute of Engineering and Technology, Patiala** (graduating 2027). I like understanding how things work under the hood, and then building my own version to prove it.

- 🌍 Open Source Software Developer at **FOSSASIA (Visdom)** since March 2026
- 🛡️ Former Joint Secretary of the **OWASP Student Chapter at TIET** (Sept 2024 – May 2026)
- 🎯 Looking for **fresher SDE roles** (Gurgaon / Bangalore), especially backend and distributed systems
- 📚 Currently going deep on compiler design

---

## 🚀 Featured project: [GFS](https://github.com/Lord-OfShadows/gfs)

A **Google File System-inspired distributed file system** written in Go. I learned Go while building it.

**Architecture:** one coordinator for metadata, four chunkservers for data, a Go CLI client, gRPC + Protobuf, and Docker Compose to run it all.

| What it does | How |
|---|---|
| Splits files into **4 MiB chunks** | Each chunk is stored on **3 replicas** |
| Replicates writes | Client → first replica → forwarding chain |
| Guarantees integrity | **SHA-256** per chunk, verified end to end |
| Detects failures | **1 s heartbeats**, nodes marked Suspect then Unavailable |
| Heals itself | Automatic re-replication with a bounded worker pool |

**Measured, not claimed** (one laptop, Docker Compose, 20 MB file, one chunkserver stopped, 20 runs):

- ⏱️ Failure detected in **2.8 s** median
- 🔧 Repair finished in **0.6 s** median
- ✅ Back to 3 copies in **3.4 s** median, and **20/20 runs succeeded**
- 📖 Reads keep working with **2 of 4 nodes down**
- 🔁 **2.48 GB** round trip, byte-identical

**Design principles I followed:**

- Metadata plane kept separate from the data plane
- Explicit state machines and typed errors instead of boolean flags
- Timeouts mean *suspicion*, not certainty
- Idempotent repair tasks, every RPC has a deadline
- Never hold a lock during network or disk I/O

**What I want to do next:** persist coordinator metadata across restarts, fix the read stall on a just-died replica, and pipeline writes instead of store-and-forward. The open issues are documented in the repo, including the known limitations.

---

## 🤖 Machine learning

- Studied and built with **CNN, RNN, LSTM, GRU**
- Fine-tuned **Whisper with LoRA**
- Built a **dysarthric speech** project using **HuBERT with LoRA** optimization
- Exploring **RAG / GenAI** and multi-tenant LoRA adapter serving for what comes next

---

## 🛠️ Tech stack

<p>
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="C++">
  <img src="https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white" alt="Go">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React">
  <img src="https://img.shields.io/badge/gRPC-244C5A?style=for-the-badge&logo=grpc&logoColor=white" alt="gRPC">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch">
</p>

---

## 🎯 What I'm working toward

- Landing a backend / systems SDE role where I can work on problems around reliability and scale
- Contributing more to open source through FOSSASIA
- Building an ML project that has real impact, not just a notebook
- Turning every project into a "found it, fixed it, measured it" story

---

## 🎮 Outside of code

Reading, football, and a lot of Bloodborne and Fortnite.

---

<p align="center">
  <i>If you're hiring, building something interesting, or just want to talk systems, reach out on <a href="https://www.linkedin.com/in/arjunangirus">LinkedIn</a>.</i>
</p>
