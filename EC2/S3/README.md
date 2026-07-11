# Amazon S3 (Simple Storage Service)

## What is Amazon S3?

Amazon S3 (Simple Storage Service) is a cloud storage service provided by Amazon Web Services (AWS). It allows users to securely store and retrieve files from anywhere in the world.

Files stored in Amazon S3 are called **objects**, and they are stored inside **buckets**.

## Key Features

- Highly durable and reliable storage
- Secure data storage with encryption
- Scalable storage that grows as your data grows
- Easy access from anywhere using the internet
- Supports versioning to recover deleted or modified files

## Common Use Cases

- Storing images and videos
- Hosting static websites
- Backing up important files
- Storing application data
- Disaster recovery and archiving

## S3 Storage Classes

Amazon S3 provides different storage classes to meet different needs:

- **S3 Standard** – Frequently accessed data
- **S3 Intelligent-Tiering** – Automatically moves data to the most cost-effective storage tier
- **S3 Standard-IA** – Infrequently accessed data
- **S3 One Zone-IA** – Infrequently accessed data stored in a single Availability Zone
- **S3 Glacier Instant Retrieval** – Archived data that needs quick access
- **S3 Glacier Flexible Retrieval** – Long-term archive storage
- **S3 Glacier Deep Archive** – Lowest-cost storage for long-term backups

## Benefits of Amazon S3

- High availability
- Excellent durability (99.999999999% or 11 nines)
- Cost-effective
- Easy to scale
- Strong security features

## What I Learned

- Amazon S3 is an object storage service.
- Data is stored in buckets as objects.
- Buckets must have globally unique names.
- Amazon S3 is ideal for backups, static websites, and storing files.
- Different storage classes help reduce storage costs.

## Hands-on Practice

- Created my first S3 bucket.
- Uploaded files to an S3 bucket.
- Explored bucket permissions.
- Learned about S3 storage classes.
