<h1 align="center">
🚀  Export Data from BigQuery to Cloud Storage
 ||       🚀
</h1>

### **Solution Video:** [Watch Here]()

### Task 1

```lookml

bq load --source_format=CSV --autodetect customer_details.customers customers.csv ;

bq query --use_legacy_sql=false --destination_table customer_details.male_customers 'SELECT CustomerID, Gender FROM customer_details.customers WHERE Gender="Male"' ;

PROJECT_ID=$(gcloud config get-value project) ;

bq extract customer_details.male_customers gs://$PROJECT_ID-bucket/exported_male_customers.csv ;

bq query --use_legacy_sql=false --replace --destination_table=customer_details.male_customers 'SELECT CustomerID, Gender FROM customer_details.customers WHERE Gender = "Male"' ;

```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
