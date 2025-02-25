Object:S3/MaliciousFile
-----------------------

### A malicious file has been detected on a scanned S3 object.

**Default severity: High**

* **Feature:** Malware Protection for S3

This finding indicates that a malware scan has detected the listed S3 object to be malicious. For more information, view the **Threats detected** section in the finding details panel.

**Recommendation remediation:**

If this finding was unexpected, the S3 object is potentially malicious. For information about recommended remediation steps, see [Remediating a potentially malicious S3 object](https://docs.aws.amazon.com/guardduty/latest/ug/compromised-s3object-malware-protection-gdu.html).