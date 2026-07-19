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
