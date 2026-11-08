# AWS S3 Infrastructure Setup

## 1. Project Overview

This document describes the AWS S3 infrastructure setup for the High-Traffic Middle East E-Commerce Flash Sale Analytics Pipeline.

The purpose is to provide secure and organized cloud storage for flash-sale event data.

## 2. AWS Configuration

| Setting | Value |
|---|---|
| AWS Service | Amazon S3 |
| AWS Region | US East (N. Virginia) |
| Region Code | us-east-1 |
| Bucket Name | me-flash-sale-data-lake-2026-01 |
| Bucket Type | General Purpose |
| Object Ownership | Bucket owner enforced |

## 3. S3 Data Lake Structure

The following folder structure was created inside the S3 bucket:

```text
me-flash-sale-data-lake-2026-01/
├── raw/
├── curated/
└── results/
```

### Folder Description

- **raw/**: Stores original, unprocessed event data.
- **curated/**: Stores cleaned and processed datasets.
- **results/**: Stores analytical outputs and generated results.

## 4. Security Configuration

### 4.1 Block Public Access

Block all public access: **Enabled**

All four public access blocking settings are enabled to prevent unintended public access to the bucket and its objects.

### 4.2 Default Encryption

Encryption type: **Server-side encryption with Amazon S3 managed keys (SSE-S3)**.

Default encryption is enabled to protect newly uploaded objects at rest.

## 5. Implementation Status

| Task | Status |
|---|---|
| Create S3 bucket | Completed |
| Create raw/ prefix | Completed |
| Create curated/ prefix | Completed |
| Create results/ prefix | Completed |
| Enable default encryption | Completed |
| Enable Block Public Access | Completed |

## 6. S3 Bucket Information

**Bucket URI:**

`s3://me-flash-sale-data-lake-2026-01/`

**Region:** `us-east-1`

## 7. Conclusion

The AWS S3 data lake infrastructure has been successfully created and configured.

The bucket is protected with default server-side encryption and Block Public Access. The required folder structure is ready for the next stage of the project, which involves dataset generation and data ingestion.

## 8. Implementation Evidence

The following screenshots demonstrate the successful AWS S3 configuration.

### 8.1 S3 Bucket Structure
![S3 Bucket Structure](screenshots/s3-bucket-structure.png)

### 8.2 Block Public Access
![S3 Public Access](screenshots/s3-public-access.png)

### 8.3 Default Encryption
![S3 Encryption](screenshots/s3-encryption.png)
