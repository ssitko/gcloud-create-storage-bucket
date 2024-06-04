# gcloud storage create bucket

This repository contains Github action for creating google _storage_ buckets using **gcloud** utility.

# how to use

1. Make sure that **google-github-actions/auth** and **google-github-actions/setup-gcloud** actions are running before this github action in your manifest
2. Add following lines to you github action:

your-gh-manifest.yaml

```
- name: Use gcloud storage create bucket action
  uses: ssitko/gcloud-create-storage-bucket@v0.1
  with:
    project-id: your-project-id
    bucket-name: your-topic-name
    storage-type: COLDLINE // this is optional, it deaults to STANDARD if not provided
    notification-topic: topic-name // this is optional, but if provided, must be defined with event-type parameter
    event-type: OBJECT_FINALIZE
```

### Szymon Sitko @ 2024
