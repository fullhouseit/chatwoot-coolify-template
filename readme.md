# Chatwoot Self-Hosted docker compose for Coolify

This is a modified copy of compose file in Coolify repo with enabled active storage.

Original template: https://github.com/coollabsio/coolify/blob/b2bab451d3a28c973807ab306931c279a4d88ab5/templates/compose/chatwoot.yaml

- Coolify docs: https://coolify.io/docs/
- Chatwoot docs: https://www.chatwoot.com/docs/self-hosted

## Configure S3 compatible storage

You can use any S3 compatible provider or Minio. For usage of Amazon S3, Google GCS, Microsoft Azure, please refer to [documentation](https://www.chatwoot.com/docs/self-hosted/deployment/storage/supported-providers), you will need to modify docker compose to add required environment variables.

```
ACTIVE_STORAGE_SERVICE=s3_compatible
STORAGE_BUCKET_NAME=
STORAGE_ACCESS_KEY_ID=
STORAGE_SECRET_ACCESS_KEY=
STORAGE_REGION=nyc3
STORAGE_ENDPOINT=https://nyc3.digitaloceanspaces.com
#set force_path_style to true if using minio
#STORAGE_FORCE_PATH_STYLE=true
```