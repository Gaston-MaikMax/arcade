<h1 align="center">
🚀  Derive Insights from BigQuery Data: Challenge Lab
 || GSP787       🚀
</h1>

### **Solution Video:** [Watch Here]()

### Task 1

```lookml

curl -LO raw.githubusercontent.com/prateekrajput08/Arcade-Google-Cloud-Labs/refs/heads/main/Derive%20Insights%20from%20BigQuery%20Data%3A%20Challenge%20Lab/TechCode.sh
sudo chmod +x TechCode.sh
./TechCode.sh

```

### Task 2

```lookml


SELECT
  DATE(date) AS date
FROM (
  SELECT
    date,
    SUM(cumulative_deceased) AS total_deaths
  FROM
    `bigquery-public-data.covid19_open_data.covid19_open_data`
  WHERE
    country_name = 'Italy'
    AND date >= '2020-01-01'
  GROUP BY
    date
)
WHERE
  total_deaths > 10000
ORDER BY
  date ASC
LIMIT 1;

```

### Kudos 🌟 on completing the lab!

#### You’ve brilliantly showcased your talent and dedication.

### Keep it up!

### don't forget to follow [here](https://youtube.com/@hellodev1?si=1GE3_P0V8xbViLhc)
