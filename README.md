# SQL Injection DoS – Server Crash Visualization Dashboard

An interactive and educational cyber-security dashboard that demonstrates how **SQL Injection-based Denial-of-Service (DoS) attacks** can degrade or crash database servers through **resource exhaustion techniques**.

This tool detects malicious SQL patterns, generates visual performance impact data, compares malicious vs. safe queries, and provides **automatic sanitization with defense recommendations** for secure database applications.

---

## 🚀 Features

| Capability | Description |
|-----------|-------------|
| **Malicious SQL Detection** | Identifies DoS-driven injection patterns such as BENCHMARK, SLEEP, recursive CTEs, nested joins, etc. |
| **Impact Prediction Engine** | Auto-generates CPU, Memory, Response Time, and Connection utilization curves. |
| **Performance Charts** | Visual comparison between malicious queries vs. normal queries (Chart.js). |
| **Sanitized Query Generator** | Automatically transforms malicious payloads into safe, parameterized SQL. |
| **Defense Recommendations** | Includes mitigations like query timeouts, least-privilege DB users, WAF, input validation, etc. |
| **Real-Time Risk Classification** | Displays severity labels (Medium/High/Critical) with explanations. |

---

## 📸 Demo Overview

The dashboard includes:

- Query input panel (malicious + normal)
- DoS threat classification with pattern-based reasoning
- Auto-generated performance metrics
- Multi-tab interface for Overview, Charts, Analysis, and Defense
- Sanitized SQL generation + list of applied mitigation steps

---

## 🧠 How It Works

1. User inputs a malicious SQL payload.
2. The query is scanned for known DoS patterns.
3. Each pattern contributes to an **Impact Score (0–100)** based on severity.
4. Metrics are generated to simulate server behavior over time.
5. Data is visualized with interactive charts comparing:
   - CPU usage
   - Memory usage
   - Response time
   - Active DB connections
6. A secure, parameterized version of the query is produced, while listing all sanitization steps.

---

## 🛡️ Supported Attack Pattern Detection

| Attack Technique | Result |
|------------------|--------|
| `BENCHMARK()` | CPU exhaustion |
| `SLEEP()` / `WAITFOR DELAY` | Thread starvation & latency DoS |
| Recursive CTE | Infinite / heavy memory allocation |
| Cartesian product joins | Exponential result set growth |
| `UNION SELECT stacking` | Query amplification |
| `RANDOMBLOB()` | Memory bloat |
| `LOAD_FILE()` | Disk I/O saturation |
| `REPEAT()` | Memory & string buffer flooding |

Each matched pattern includes a warning, severity indicator, and explanation of its impact.

---

## 🛑 Disclaimer

This project is designed purely for **education and academic security research**.  
Do **not** deploy malicious queries against real production systems.  
Use responsibly and lawfully.

---



## 📄 License

This project is licensed under the **MIT License** unless the repository owner chooses otherwise.

