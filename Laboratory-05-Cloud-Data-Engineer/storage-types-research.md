# Research: Types of Cloud Storage

## Introduction

Cloud storage allows users and applications to store and access data. The three main types are Block Storage, File Storage, and Object Storage. Each type is designed for different workloads.

## Comparison of Cloud Storage Types

| Storage Type | Description | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| Block Storage | Divides data into fixed-sized blocks that can be managed separately. | Virtual machine disks, databases, and operating systems. | Amazon Elastic Block Store (Amazon EBS) |
| File Storage | Organizes data into files and folders using a hierarchical structure. | Shared folders, team documents, and applications that need shared file access. | Amazon Elastic File System (Amazon EFS) |
| Object Storage | Stores data as objects containing the data, metadata, and a unique identifier. | Images, videos, backups, and other unstructured data. | Amazon Simple Storage Service (Amazon S3) |

## Recommendation to the Client

Object Storage is the best choice for the client's photo-sharing application because it is designed to store large amounts of unstructured data, such as user-uploaded images. Each image can be stored as an individual object and accessed through an application or API. Object storage services can also scale to support growing collections of photos without requiring the application to store the images inside its web server container.

## Sources

- Amazon Web Services. (n.d.). Amazon EBS. https://aws.amazon.com/ebs/
- Amazon Web Services. (n.d.). Amazon EFS. https://aws.amazon.com/efs/
- Amazon Web Services. (n.d.). Amazon S3. https://aws.amazon.com/s3/
