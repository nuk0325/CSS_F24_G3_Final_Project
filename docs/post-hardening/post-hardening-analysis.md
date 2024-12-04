# Post-Hardening Analysis

## Vulnerability Comparison

| Vulnerability Family   | Pre-Hardening (Joshua's Scan) | Post-Hardening (My Scan) | Status       |
|------------------------|------------------------------|--------------------------|--------------|
| Web Servers            | 5                            | 6                        | Increased    |
| General                | 8                            | 11                       | Increased    |
| Service Detection      | 4                            | 4                        | Unchanged    |
| Miscellaneous          | 2                            | 2                        | Unchanged    |

## Key Findings

1. **Persisting Vulnerabilities:**
   - OpenSSH vulnerabilities remain, despite applying updates.
   - SSL self-signed certificate issue persists, requiring further action.

2. **Newly Detected Issues:**
   - Increased detection in "Web Servers" and "General" categories post-hardening.
   - These may be due to updated scanning methodologies or configurations.

## Conclusion

While the overall vulnerability count decreased, the hardening process highlighted areas for continuous improvement. Future steps include upgrading software versions, replacing self-signed SSL certificates, and addressing service misconfigurations.
