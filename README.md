# UE23CS351B - Cloud Computing 
## Lab 2 - Monolithic Architecture
### Name: AKHILESH ANIL
### SRN: PES1UG23CS045
### Class & Section: 6th Semester, 'A' Section, B.Tech. CSE, PES University
#### Date: 29th January 2026, Thursday

## Performance Optimization Results
### `/events` (SS6 & SS7)
#### Metrics

| Metric                    | Before Optimization | After Optimization |
|---------------------------|---------------------|-------------------|
| Avg. Response Time (ms)   | 252.5               | 119.35            |
| Requests / Second         | 0.62                | 0.66              |

#### Analysis
- **What was the bottleneck?**  
  A CPU-wasting loop named `waste` (a `for` loop with 3,000,000 iterations) existed inside the request handler.
- **What change did you make?**  
  The unnecessary loop was removed.
- **Why did the performance improve?**  
  Eliminating redundant CPU work reduced request latency and increased overall throughput.

---

### `/myevents` (SS8 & SS9)
#### Metrics
| Metric                    | Before Optimization | After Optimization |
|---------------------------|---------------------|-------------------|
| Avg. Response Time (ms)   | 176.85              | 115.08            |
| Requests / Second         | 0.65                | 0.65              |

#### Analysis
- **What was the bottleneck?**  
  Similar to the `/events` endpoint, a CPU-wasting loop named `dummy` (a `for` loop with 1,500,000 iterations) was present inside the handler.
- **What change did you make?**  
  The loop was removed.
- **Why did the performance improve?**  
  By avoiding pointless iterations, CPU time per request was reduced, resulting in improved response time.
