# GIntroduction to Cloud Dataproc: Hadoop and Spark on Google Cloud || GSP123 ||

### **Solution Video:** [Watch Here](https://youtu.be/sj0lhJxVpeM)

### Task 1. Create a chat app from a template

### Step 1 .

```
# Prompt user for input
echo "Enter the region:"
read REGION
echo "Enter the zone:"
read ZONE
echo "Enter the project ID:"
read PROJECT_ID

# Create Dataproc cluster
gcloud dataproc clusters create qlab \
  --enable-component-gateway \
  --region $REGION \
  --zone $ZONE \
  --master-machine-type e2-standard-4 \
  --master-boot-disk-type pd-balanced \
  --master-boot-disk-size 100 \
  --num-workers 2 \
  --worker-machine-type e2-standard-2 \
  --worker-boot-disk-size 100 \
  --image-version 2.2-debian12 \
  --project $PROJECT_ID


```

### Step 2 .

```
# Prompt user for input
echo "Enter the region:"
read REGION

# Submit Spark job to the cluster
gcloud dataproc jobs submit spark \
  --region $REGION \
  --cluster qlab \
  --class org.apache.spark.examples.SparkPi \
  --jars file:///usr/lib/spark/examples/jars/spark-examples.jar \
  -- 1000



```

PLEASE SUBSCRIBE 😸

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
