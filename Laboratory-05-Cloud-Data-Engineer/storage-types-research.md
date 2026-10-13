## Storage Types Research

### Cloud Storage Comparison

| Storage type | How it stores data | Best used for | Cloud provider example |
|---|---|---|---|
| Block storage | Splits data into raw, fixed-size blocks, each with its own address. It works like a raw hard drive attached to an operating system or virtual machine. | Databases, boot volumes, and transactional workloads that need low-latency reads and writes. | AWS EBS (Elastic Block Store) |
| File storage | Keeps data in a hierarchy of files and folders, like a desktop directory or a network-attached storage (NAS) device. | Shared team directories, home directories, content management systems, and collaborative file editing. | AWS EFS (Elastic File System) |
| Object storage | Stores each piece of data as an object that bundles the data, its metadata, and a unique global identifier. Objects sit in a flat structure inside buckets, not folders. | Large amounts of unstructured data, such as user-uploaded images, video backups, logs, and static web assets. | AWS S3 (Simple Storage Service) |

### Why object storage suits user-uploaded images

I would use object storage for the client's photo-sharing app. It is built to handle millions of unstructured files like images at a reasonable cost. Block and file storage get slower or more expensive once a directory holds millions of files. Object storage avoids that problem because it uses a flat namespace and metadata tags, so files can be retrieved quickly and the system keeps scaling. Containers and web servers are also temporary, which means the images have to be stored somewhere else. With object storage, uploaded photos stay safe and available even when the application servers are replaced.
