# Troubleshooting Guide

## Service profile cannot be activated

### Symptom

A service profile remains in the **Pending** state after activation is requested.

### Possible causes

- A required configuration value is missing.
- A dependent service is unavailable.
- The profile contains an unsupported value.
- The activation request failed validation.

### Resolution

1. Open the service profile.
2. Review the validation status.
3. Confirm that all mandatory fields contain valid values.
4. Check the status of dependent services.
5. Correct any reported configuration errors.
6. Retry activation.

### If the issue persists

Collect the following information before escalating the issue:

- Service profile ID
- Approximate time of the failed activation
- Error message
- Relevant application logs
- Steps already performed

Providing these details helps reduce back-and-forth during troubleshooting.

## Troubleshooting writing principles

A useful troubleshooting topic should clearly separate:

- Symptom: what the reader observes.
- Cause: why the issue may occur.
- Resolution: what the reader should do.
- Escalation information: what evidence should be collected if the resolution does not work.
