# Laboratory Activity 5: The Cloud Data Engineer

## Mission Overview
This laboratory covers the configuration and deployment of an S3-compatible Object Storage server using MinIO on Docker. The deployment establishes a dedicated, scalable storage layer for unstructured image data to keep application web containers stateless.

## Objectives
- Differentiate between Block, File, and Object Storage.
- Deploy an S3-compatible Object Storage server (MinIO) using Docker.
- Access a cloud service via a web interface using port forwarding.
- Create a storage bucket and upload objects (files) to the cloud.
- Document cloud storage operations using Markdown.
- Continue expanding a professional GitHub Cloud Computing Portfolio. 

## Tools Used
- **Environment:** KillerCoda Ubuntu Playground
- **Engine:** Docker Engine
- **Storage Software:** MinIO (S3-Compatible Object Store)
- **Version Control:** Git & GitHub
- **Documentation:** Markdown

## Skills Learned
- Configuring multi-port container publishing (`9000` API, `9001` Web Console).
- Injecting container secrets and credentials via environment variables (`-e`).
- Managing object lifecycles and bucket namespaces.
- Decoupling persistent object storage from containerized application runtimes.
