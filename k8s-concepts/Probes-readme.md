ReadinessProbes and LivenessProbes will be executed periodically all the time.

If a StartupProbe is defined, ReadinessProbes and LivenessProbes won't be executed until the StartupProbe succeeds.

ReadinessProbe fails*: Pod won't be marked Ready and won't receive any traffic

LivenessProbe fails*: The container inside the Pod will be restarted

StartupProbe fails*: The container inside the Pod will be restarted

*fails: fails more times than configured with failureThreshold