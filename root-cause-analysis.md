# Root Cause Analysis

## Database Metrics

| Time | CPU | Response Time |
|------|-----|--------------|
| 10:00 | 25% | 50ms |
| 10:05 | 75% | 500ms |
| 10:10 | 95% | 3000ms |

## Findings

Database CPU usage increased rapidly.

High query latency caused application timeouts.

This resulted in service failures across dependent microservices.

---

## Cascading Failure

Database Slowdown
↓
Authentication Service Failure
↓
Payment Service Failure
↓
API Gateway Timeout
↓
Customer Outage

## Conclusion

The database performance degradation triggered a chain reaction across multiple services, ultimately causing a complete application outage.