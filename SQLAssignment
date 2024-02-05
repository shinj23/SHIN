1. Total Number of Transactions:
```SQL
SELECT COUNT(*) AS total_transactions
FROM `bigquery-public-data.crypto_bitcoin.transactions`;
```


![image](https://github.com/shinj23/SHIN/assets/159032176/ba0cb753-3a87-47fa-8a0f-0aaef7c9ea0e)


2. Average Transaction Fee:
```SQL
SELECT AVG(fee) AS avg_transaction_fee
FROM `bigquery-public-data.crypto_bitcoin.transactions`;
```


![image](https://github.com/shinj23/SHIN/assets/159032176/95fffa85-c662-4417-8798-ab4e081e44c7)

3. Bitcoin Received per Day:
```SQL
SELECT DATE(block_timestamp) AS date,
       SUM(output_value) AS bitcoin_received
FROM `bigquery-public-data.crypto_bitcoin.transactions`
GROUP BY date
ORDER BY date;
```


![image](https://github.com/shinj23/SHIN/assets/159032176/c7ad72d6-3793-4b16-a5c2-632843ebff74)

4. Bitcoin Sent per Day:
```SQL
SELECT DATE(block_timestamp) AS date,
       SUM(input_value) AS bitcoin_sent
FROM `bigquery-public-data.crypto_bitcoin.transactions`
GROUP BY date
ORDER BY date;
```


![image](https://github.com/shinj23/SHIN/assets/159032176/a5e66e9a-6086-4d85-9369-558bfb7a8e24)

5. Distribution of Transaction Sizes:
```SQL
SELECT ROUND(output_value, -5) AS transaction_size_range,
       COUNT(*) AS num_transactions
FROM `bigquery-public-data.crypto_bitcoin.transactions`
GROUP BY transaction_size_range
ORDER BY transaction_size_range;
```


![image](https://github.com/shinj23/SHIN/assets/159032176/b86b546b-c3ae-4f82-8510-d2dbccf6e3a5)

6. Top 5 Days with Highest Transaction Fees:
```SQL
SELECT DATE(block_timestamp) AS date,
       SUM(fee) AS total_transaction_fees
FROM `bigquery-public-data.crypto_bitcoin.transactions`
GROUP BY date
ORDER BY total_transaction_fees DESC
LIMIT 5;
```


![image](https://github.com/shinj23/SHIN/assets/159032176/43ddfaac-0a24-441e-9817-198f516e3805)

7. Top 5 Days with Highest Bitcoin Volume Transferred:
```SQL
SELECT DATE(block_timestamp) AS date,
       SUM(output_value) AS total_bitcoins_transferred
FROM `bigquery-public-data.crypto_bitcoin.transactions`
GROUP BY date
ORDER BY total_bitcoins_transferred DESC
LIMIT 5;
```


![image](https://github.com/shinj23/SHIN/assets/159032176/d42e3742-f7c9-4ae1-84b1-fbc31cca7a3b)

8. Distribution of Block Sizes:
```SQL
SELECT ROUND(size, -5) AS block_size_range,
       COUNT(*) AS num_blocks
FROM `bigquery-public-data.crypto_bitcoin.blocks`
GROUP BY block_size_range
ORDER BY block_size_range;
```


![image](https://github.com/shinj23/SHIN/assets/159032176/50999369-4a25-451b-bfd2-9e4ee262faa1)

9. Join on Country and Region Code:
```SQL
SELECT p.*, r.*
FROM `bigquery-public-data.covid19_italy_eu.data_by_province` AS p
LEFT JOIN `bigquery-public-data.covid19_italy_eu.data_by_region` AS r
ON p.country = r.country AND p.region_code = r.region_code;
```


![image](https://github.com/shinj23/SHIN/assets/159032176/daa93791-0c8e-4e64-b4f6-93a9a4165473)

10. Join on Date and Province Code:
```SQL
SELECT p.*, r.*
FROM `bigquery-public-data.covid19_italy_eu.data_by_province` AS p
LEFT JOIN `bigquery-public-data.covid19_italy_eu.data_by_region` AS r
ON p.date = r.date AND p.province_code = r.region_code;
```


![image](https://github.com/shinj23/SHIN/assets/159032176/2e81b863-7703-450d-ae2f-b4f5e4209e3e)
