# ITC 6050 — Week 1 Lab

## Concept Checks

### Step 1 — Why Docker instead of a native Postgres install?
Running PostgreSQL in Docker ensures every student uses the exact same version in an isolated environment, eliminating "works on my machine" conflicts with other software.

### Step 3 — What did dlt do that plain Python + SQLAlchemy would not?
1. Automatically inferred and created the Postgres table schema from the API response
2. Handled pagination of the GitHub API automatically
3. Managed the loading process including error handling and load tracking

### Step 4 — How did dlt handle nested JSON fields like user and labels?
dlt automatically flattened nested JSON objects into columns (e.g., user__login) and stored JSON arrays as JSONB columns in Postgres, handling complex nested structures without any manual schema definition.