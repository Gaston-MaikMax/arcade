<h1 align="center">
🚀  Introduction to Cloud Dataproc: Hadoop and Spark on Google Cloud
 || GSP123   🚀
</h1>

### **Solution Video:** [Watch Here]()

### Task 1.

```lookml

export CLUSTER_NAME=

```

### Task 2.

```lookml

gcloud auth list

export ZONE=$(gcloud compute project-info describe --format="value(commonInstanceMetadata.items[google-compute-default-zone])")
export REGION=$(gcloud compute project-info describe --format="value(commonInstanceMetadata.items[google-compute-default-region])")

PROJECT_NUMBER=$(gcloud projects describe $(gcloud config get-value project) --format="value(projectNumber)")

gcloud projects add-iam-policy-binding $DEVSHELL_PROJECT_ID \
    --member="serviceAccount:$PROJECT_NUMBER-compute@developer.gserviceaccount.com" \
    --role="roles/storage.admin"

```

### Task 3.

```lookml

# Function to create the Dataproc cluster
cluster_function() {
  gcloud dataproc clusters create "$CLUSTER_NAME" \
    --region "$REGION" \
    --zone "$ZONE" \
    --master-machine-type n1-standard-2 \
    --worker-machine-type n1-standard-2 \
    --num-workers 2 \
    --worker-boot-disk-size 100 \
    --worker-boot-disk-type pd-standard \
    --no-address
}

cp_success=false

while [ "$cp_success" = false ]; do
  cluster_function
  exit_status=$?

  if [ "$exit_status" -eq 0 ]; then
    cp_success=true
  else
    if gcloud dataproc clusters describe "$CLUSTER_NAME" --region "$REGION" &>/dev/null; then
      gcloud dataproc clusters delete "$CLUSTER_NAME" --region "$REGION" --quiet
      sleep 10
    else
      sleep 10
    fi
  fi
done

# Submit Spark job
gcloud dataproc jobs submit spark \
    --project "$DEVSHELL_PROJECT_ID" \
    --region "$REGION" \
    --cluster "$CLUSTER_NAME" \
    --class org.apache.spark.examples.SparkPi \
    --jars file:///usr/lib/spark/examples/jars/spark-examples.jar \
    -- 1000

```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
