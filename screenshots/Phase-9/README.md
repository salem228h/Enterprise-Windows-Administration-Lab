## Application Log Investigation

Event Viewer Application Logs were reviewed.

Detected Event:
- Source: User Profile Service
- Event ID: 1512

Analysis:
Windows was unable to unload the user registry hive because memory used by the registry was not released.

Impact:
Low impact warning related to user profile cleanup during logoff.

Troubleshooting:
Reviewed running processes and documented the event for monitoring.
## Performance Monitoring

Performance Monitor was used to evaluate workstation health.

Monitored Counters:
- Processor → % Processor Time (_Total)
- Memory → Available MBytes
- PhysicalDisk → % Disk Time (_Total)

Results:
- CPU utilization remained within normal limits.
- Available memory was sufficient for normal operation.
- Disk activity showed no sustained high utilization.

Conclusion:
No immediate performance bottlenecks were detected during monitoring.
