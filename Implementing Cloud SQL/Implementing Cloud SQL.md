# Implementing Cloud SQL || ||

### **Solution Video:** [Watch Here]()

### Step 1 .

```
ZONE=$(gcloud compute instances list --filter="name=wordpress-proxy" --format "get(zone)" | awk -F/ '{print $NF}')

REGION=${ZONE::-2}

gcloud services enable servicenetworking.googleapis.com
gcloud services enable servicemanagement.googleapis.com
export PROJECT_ID=$(gcloud config list --format 'value(core.project)')

gcloud compute addresses create default-ip-rangeee \
    --global \
    --purpose=VPC_PEERING \
    --prefix-length=24 \
    --description="SQL" \
    --network=default

gcloud services vpc-peerings connect \
    --service=servicenetworking.googleapis.com \
    --ranges=default-ip-rangeee \
    --network=default

gcloud beta sql instances create wordpress-db --database-version=MYSQL_5_7 --cpu=1 --memory=3840MB --region=$REGION --root-password=password123 --network=projects/$PROJECT_ID/global/networks/default --allocated-ip-range-name=default-ip-rangeee

gcloud sql databases create wordpress --instance=wordpress-db


gcloud beta compute ssh wordpress-proxy -- -vvv

```

### Step 2 .

```
wget https://dl.google.com/cloudsql/cloud_sql_proxy.linux.amd64 -O cloud_sql_proxy && chmod +x cloud_sql_proxy

export PROJECT_ID=$(gcloud config list --format 'value(core.project)')
ZONE=$(gcloud compute instances list --filter="name=wordpress-proxy" --format "get(zone)" | awk -F/ '{print $NF}')
REGION=${ZONE::-2}
export SQL_CONNECTION=$PROJECT_ID:$REGION:wordpress-db
./cloud_sql_proxy -instances=$SQL_CONNECTION=tcp:3306 &

```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
