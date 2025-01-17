# Analyzing Findings with Security Command Center || [GSP1164]() ||

### **Solution Video:** [Watch Here]()

### Step 1 .

```
curl -LO raw.githubusercontent.com/QUICK-GCP-LAB/2-Minutes-Labs-Solutions/main/Analyzing%20Findings%20with%20Security%20Command%20Center/gsp1164-1.sh

sudo chmod +x gsp1164-1.sh

./gsp1164-1.sh

```

- Go to `Export to Pub/Sub` from [here](https://console.cloud.google.com/security/command-center/config/continuous-exports/pubsub)

- `export-findings-pubsub`

### Step 2 .

```
export ZONE=

```

### Step 3 .

```
curl -LO raw.githubusercontent.com/QUICK-GCP-LAB/2-Minutes-Labs-Solutions/main/Analyzing%20Findings%20with%20Security%20Command%20Center/gsp1164-2.sh

sudo chmod +x gsp1164-2.sh

./gsp1164-2.sh

```

### Step 4 .

```
bq query --apilog=/dev/null --use_legacy_sql=false  \
"SELECT finding_id,event_time,finding.category FROM continuous_export_dataset.findings"

```

- Got to `Create a bucket` from [here](https://console.cloud.google.com/storage/create-bucket)

- for BUCKET NAME type `scc-export-bucket-`YOUR_PROJECT_ID

- Now go to `Export findings to Cloud Storage` from [here](https://console.cloud.google.com/security/command-center/export)

- Set the filename to `findings.jsonl`

- Go to `BigQuery Studio` from [here](https://console.cloud.google.com/bigquery)

- Set the TABLE NAME to `old_findings`

- Now paste in the following schema

### Step 5 .

```
[
  {
    "mode": "NULLABLE",
    "name": "resource",
    "type": "JSON"
  },
  {
    "mode": "NULLABLE",
    "name": "finding",
    "type": "JSON"
  }
]
```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
