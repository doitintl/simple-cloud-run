## GCP Simplicity Demo - Cloud Run

```bash
gcloud builds submit  --pack image=gcr.io/${PROJECT-ID}/simple-cloud-run
```

```bash
gcloud run deploy --image gcr.io/chetz-playground/simple-cloud-run
```

