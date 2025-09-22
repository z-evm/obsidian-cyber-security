
| **Index Name**    | **Purpose**                                                      |
| ----------------- | ---------------------------------------------------------------- |
| `_audit`          | Logs user actions: searches run, logins, role changes, etc.      |
| `_configtracker`  | Tracks saved searches, dashboards, and knowledge object changes. |
| `_dsappevent`     | Deployment Server app events (app deployment to clients).        |
| `_dsclient`       | Deployment Server client activity logs.                          |
| `_dsphonehome`    | Deployment clients' phone-home check-ins (heartbeat).            |
| `_internal`       | Core Splunk logs: splunkd.log, metrics.log, etc.                 |
| `_introspection`  | System-level resource usage (CPU, memory, disk I/O).             |
| `_metrics`        | Raw metrics data from mcollect or metrics input.                 |
| `_metrics_rollup` | Summarized rollup data for metrics (used in dashboards).         |
| `_telemetry`      | Usage data collected for Splunk telemetry (can be disabled).     |
| `_thefishbucket`  | Tracks file read positions (e.g. log tailing checkpoints).       |
| `summary`         | Stores accelerated reports, data model summaries, etc.           |
| `main`            | Default index — used if no index is explicitly specified.        |
