<h1 align="center">
🚀  Manage Rendering for Cloud Storage Website Hosting
 ||        🚀
</h1>

### **Solution Video:** [Watch Here]()

### Task 1

```lookml

PROJECT=$(gcloud config get-value project) && BUCKET="$BUCKET" && gsutil setmeta -h "Content-Type:text/html" gs://${BUCKET}/index.html && gsutil setmeta -h "Content-Type:text/css" gs://${BUCKET}/style.css && gsutil setmeta -h "Content-Type:image/jpeg" gs://${BUCKET}/logo.jpg && gsutil web set -m index.html -e 404.html gs://${BUCKET} && gsutil iam ch allUsers:objectViewer gs://${BUCKET}

```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
