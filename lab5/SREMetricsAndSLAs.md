# Key Metrics for SRE and SLAs

The most common SRE metrics are:

-   **Service-Level Objectives (SLOs)** - Target thresholds for reliability and performance, like uptime, latency, error rate etc.
-   **Error Budget** - The acceptable amount of downtime before SLO is breached. Helps prioritize fixes.
-   **Mean Time to Recover/Repair (MTTR)** - The average time taken to recover from an outage or service disruption.
-   **Availabilit** - The % of time a service is accessible and operational. Commonly measured in 9s like 99.99%.
-   **Latency** - The delay between a user request and the response. Critical for usability.
-   **Throughput** - The rate at which a system can process requests. Indicates capacity.
-   **Saturation** - How "full" a service is. High saturation leads to bottlenecks.
-   **Traffic Volume** - Direct measure of load on a system based on # of requests.

_Google Cloud_ commits to **99.95%** monthly uptime for its core services like Cloud Storage, Bigtable etc. Their error budget is just **0.05%** per month.

_Amazon Web Services_ guarantees **99.99%** availability per year for resources like EC2 virtual machines. Their max error budget is **52min** of downtime annually.

These metrics and tight SLAs force reliability into the software lifecycle. Companies invest heavily in redundancy, monitoring, auto-scaling and other SRE practices to meet availability goals. Metrics provide accountability and are key to delivering robust, high-traffic services. They enable data-driven SRE and optimal user experience.
