<h1 align="center">
🚀  Data Ingestion into BigQuery from Cloud Storage
 ||        🚀
</h1>

### **Solution Video:** [Watch Here]()

### Task 1

```lookml


bq mk work_day && bq load --source_format=CSV --skip_leading_rows=1 work_day.employee gs://qwiklabs-gcp-04-d6c61a671c00-5xyr-bucket/employees.csv employee_id:INTEGER,device_id:STRING,username:STRING,department:STRING,office:STRING

```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
