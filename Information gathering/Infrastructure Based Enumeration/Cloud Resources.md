

Cloud platforms like AWS, GCP, and Azure are widely used for centralized management. Misconfigurations (e.g., open S3 buckets, Azure blobs, GCP storage) can expose sensitive data.

## Discovery Techniques

- **DNS Enumeration:** Cloud storage often appears in DNS records.
- **Google Dorks:**  
    - `intext:<company> inurl:amazonaws.com`  
    - `intext:<company> inurl:blob.core.windows.net`
- **Source Code Review:** Look for cloud storage URLs in HTML/CSS/JS.
- **Third-party Tools:**  
    - [domain.glass](https://domain.glass): Infrastructure info, security status.  
    - [GrayHatWarfare](https://buckets.grayhatwarfare.com): Search public cloud buckets/files.

## Risks

- Sensitive files (PDFs, keys, configs) may be exposed.
- Leaked SSH keys can compromise servers.

## Notes

- Companies may use abbreviations in bucket names.
- Always check for public access and misconfigurations.

---  
**References:**  
- [AWS S3](https://aws.amazon.com/s3/)  
- [Azure Blob Storage](https://azure.microsoft.com/en-us/services/storage/blobs/)  
- [GCP Cloud Storage](https://cloud.google.com/storage)  