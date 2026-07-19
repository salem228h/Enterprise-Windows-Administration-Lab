# Troubleshooting Guide

## Common Issues

### Network Connectivity

**Symptoms**

- No Internet access
- Unable to reach network resources

**Actions**

- Run `ipconfig /all`
- Verify IP address
- Verify Default Gateway
- Test connectivity using `ping`
- Verify DNS using `nslookup`

---

### Windows Firewall

**Symptoms**

- Blocked network communication

**Actions**

- Review inbound and outbound rules
- Verify rule priority
- Test connectivity after changes

---

### Event Viewer

**Symptoms**

- System or application errors

**Actions**

- Review System logs
- Review Application logs
- Record Event ID and Source
- Investigate recurring warnings

---

### Performance Issues

**Symptoms**

- Slow system performance

**Actions**

- Monitor CPU utilization
- Monitor available memory
- Monitor disk activity
- Identify abnormal resource usage

---

### BitLocker

**Symptoms**

- Encryption status unknown

**Actions**

- Verify BitLocker status
- Confirm recovery key backup
- Validate encryption configuration
