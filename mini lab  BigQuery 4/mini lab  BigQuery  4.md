# mini lab : BigQuery : 4 || []() ||

### **Solution Video:** [Watch Here]()

### Step 1 .

```
export PROJECT_ID=$(gcloud config get-value project)
export REGION=$(gcloud compute project-info describe --format="value(commonInstanceMetadata.items[google-compute-default-region])")

```

### Step 2 .

```
eexport BUCKET_NAME=

```

### Step 3 .

```
bq load --source_format=CSV --autodetect products.products_information gs://$BUCKET_NAME/products.csv
bq query --use_legacy_sql=false "CREATE SEARCH INDEX IF NOT EXISTS products.p_i_search_index ON products.products_information (ALL COLUMNS);"
bq query --use_legacy_sql=false "SELECT * FROM products.products_information WHERE SEARCH(STRUCT(), '22 oz Water Bottle') = TRUE;"

```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
