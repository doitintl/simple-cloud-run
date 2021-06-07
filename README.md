## GCP Simplicity Demo - Cloud Run

Build,Deploy,CI/CD as simple as can be

## Init config env vars
```bash
PROJECT_ID=`gcloud config get-value project`
```

## Build your code with Cloud Build (Use buildpakcs, no need for Dockerfile)
```bash
gcloud builds submit  --pack image=gcr.io/${PROJECT_ID}/simple-cloud-run
```

## Deploy on Cloud Run
```bash
gcloud run deploy --image gcr.io/${PROJECT_ID}/simple-cloud-run
```

## If you are OK with using beta, it's even simpler
```
gcloud beta run deploy simple-cloud-run --source .
```
