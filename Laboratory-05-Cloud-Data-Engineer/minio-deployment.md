# MinIO Object Storage Deployment

## 1. Overview

This activity demonstrates how to deploy an S3-compatible object storage service using Docker. MinIO provides object storage for unstructured data, such as photos, videos, and backups.

## 2. Docker Deployment Command

The following command was used to deploy the MinIO container in the KillerCoda Ubuntu environment:

```bash
sudo docker run -d \
  -p 9000:9000 \
  -p 9001:9001 \
  --name minio-server \
  -e "MINIO_ROOT_USER=cloudadmin" \
  -e "MINIO_ROOT_PASSWORD=CloudNova2026!" \
  pgsty/minio:RELEASE.2026-08-04T00-00-00Z server /data --console-address ":9001"
```

**Note:** The running container was verified to use the `pgsty/minio:RELEASE.2026-08-04T00-00-00Z` image. The command above documents the corresponding deployment configuration. The original command attempted to use `minio/minio`, but the image pull returned an authorization error.

## 3. Port Configuration

| Port | Purpose |
|---|---|
| 9000 | MinIO API endpoint for object storage operations |
| 9001 | MinIO web console for administration |

Port 9001 was intended to provide browser access through the KillerCoda port-forwarding interface. The console remained stuck on the loading screen during testing, so successful web-console access still needs to be verified.

## 4. Environment Variables

The `-e` option passes environment variables into the Docker container.

- `MINIO_ROOT_USER=cloudadmin` specifies the root username used for MinIO administration.
- `MINIO_ROOT_PASSWORD=CloudNova2026!` specifies the root password used for authentication.

These variables configure the initial administrator credentials. In a production environment, credentials should be stored securely rather than written directly in shell commands or public documentation.

## 5. Container Verification

The following command was used to inspect the container:

```bash
sudo docker ps -a --filter name=minio-server
```

The output showed the container named `minio-server` with an `Up` status and port mappings for ports 9000 and 9001.

## 6. Bucket Configuration

**Required bucket name:** `client-photos`

The bucket is intended to store sample images for a photo-sharing application. Bucket creation and file upload must be verified in the MinIO web console before they can be reported as completed.

## 7. Conclusion

This activity provided practice with Docker deployment, port mapping, environment variables, container verification, and object storage concepts. Further testing is required to confirm that the web console is accessible and that the bucket and uploaded object are working correctly.
