# Exchange-rate-website
# System Designation - Feature 1

## Part A Business Documentation

### 1 Short Summary

Store and provide real-time exchange rates of various currencies against a base currency, and store historical exchange rate information.

### 2 Explain the Action

- A scheduled task periodically retrieves real-time exchange rate data from a third-party service and saves it to the database.
- Expose APIs for querying real-time and historical exchange rates to other services.

### 3 Explain the Outcome

- Persistent storage of exchange rate information in database.
- Provide exchange rate information for a specific point in time.

### 4 Definition of Done

- The API can correctly return exchange rate information relative to the base currency based on the specified time and currency.

- Accurately persist historical exchange rate data.

## Part B Solution Documentation

### 1 Database

Using MySQL as the database.

Currency Table

| Column        | Desription       |
| ------------- | ---------------- |
| id            | Primary Key, int |
| Currency_name | varchar(100)     |

Exchange Rate Table

| Column        | Desription       |
| ------------- | ---------------- |
| id            | Primary key, int |
| Current_id    | Foreign key      |
| Exchange_rate | Double           |
| created_time  |                  |
| Update_time   |                  |

### 2 API