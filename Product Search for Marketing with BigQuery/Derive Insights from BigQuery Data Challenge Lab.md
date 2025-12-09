<h1 align="center">
🚀  Product Search for Marketing with BigQuery
 ||       🚀
</h1>

### **Solution Video:** [Watch Here]()

### Task 1

```lookml


bq load --source_format=CSV --skip_leading_rows=1 --autodetect products.products_information gs://qwiklabs-gcp-04-2ca0d3863f4c-bucket/products.csv

```

### Task 2

```lookml

bq query --use_legacy_sql=false 'CREATE SEARCH INDEX product_search_index ON products.products_information(ALL COLUMNS)'

```

### Task 3

```lookml

bq query --use_legacy_sql=false 'SELECT * FROM products.products_information WHERE SEARCH(products_information, "22 oz Water Bottle")'

```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
