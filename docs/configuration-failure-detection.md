# Configuration: failure detection

`orchestrator` will detect failures to your topology, always. As a matter of configuration you may set the polling frequency and specific ways for `orchestrator` to notify you on such detection.

Recovery is discussed in [configuration: recovery](configuration-recovery.md)

```json
{
  "RecoveryPollSeconds": 5,
  "FailureDetectionPeriodBlockMinutes": 60,
}
```

In the above `orchestrator` will run detection every `5` seconds.

`FailureDetectionPeriodBlockMinutes` is an anti-spam mechanism that blocks `orchestrator` from notifying the same detection again and again and again.

### Hooks

Configure `orchestrator` to take action on discovery:

```json
{
  "OnFailureDetectionProcesses": [
    "echo 'Detected {failureType} on {failureCluster}. Affected replicas: {countReplicas}' >> /tmp/recovery.log"
  ],
}
```

There are many magic variables (as `{failureCluster}`, above) that you can send to your external hooks. See full list in [Topology recovery](topology-recovery.md)
